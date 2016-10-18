---
title: "Visualizer Architecture"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: na
ms.topic: "article"
dev_langs: 
  - "FSharp"
  - "VB"
  - "CSharp"
  - "C++"
ms.assetid: 6aad395f-7170-4d9e-b2b8-a5faf453380e
caps.latest.revision: 17
ms.author: "mikejo"
manager: "ghogen"
translation.priority.ht: 
  - "cs-cz"
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "pl-pl"
  - "pt-br"
  - "ru-ru"
  - "tr-tr"
  - "zh-cn"
  - "zh-tw"
---
# Visualizer Architecture
The architecture of a debugger visualizer has two parts:  
  
-   The *debugger side* runs within the Visual Studio debugger. The debugger-side code creates and displays the user interface for your visualizer.  
  
-   The *debuggee side* runs within the process Visual Studio is debugging (the *debuggee*).  
  
 A visualizer is a debugger component that enables the debugger to display (*visualize*) the contents of a data object in a meaningful, understandable form. Some visualizers support editing of the data object also. By writing custom visualizers, you can extend the debugger to handle your own custom data types.  
  
 The data object to be visualized resides within the process you are debugging (the *debuggee* process). The user interface that will display the data is created within the Visual Studio debugger process:  
  
|Debugger Process|Debuggee Process|  
|----------------------|----------------------|  
|Debugger user interface (DataTips, Watch Window, QuickWatch)|Data Object to be visualized|  
  
 To visualize the data object within the debugger interface, you need code to communicate between the two processes. Consequently, the visualizer architecture consists of two parts: *debugger side* code and *debuggee side* code.  
  
 The debugger-side code creates its own user interface, which can be invoked from the debugger interface, such as a DataTip, the Watch Window, or QuickWatch. The visualizer interface is created by using the <xref:Microsoft.VisualStudio.DebuggerVisualizers.DialogDebuggerVisualizer> class and the <xref:Microsoft.VisualStudio.DebuggerVisualizers.IDialogVisualizerService> interface. Like all Visualizer APIs, DialogDebuggerVisualizer and IDialogVisualizerService are found in the <xref:Microsoft.VisualStudio.DebuggerVisualizers> namespace.  
  
|Debugger Side|Debuggee Side|  
|-------------------|-------------------|  
|DialogDebuggerVisualizer Class<br /><br /> IDialogVisualizerService Interface|Data Object|  
  
 The user interface gets the data to be visualized from an Object Provider, which exists on the debugger side:  
  
|Debugger Side|Debuggee Side|  
|-------------------|-------------------|  
|DialogDebuggerVisualizer Class<br /><br /> IDialogVisualizerService Interface|Data Object|  
|Object Provider (implements <xref:Microsoft.VisualStudio.DebuggerVisualizers.IVisualizerObjectProvider>)||  
  
 There is a corresponding object on the debuggee side called the Object Source:  
  
|Debugger Side|Debuggee Side|  
|-------------------|-------------------|  
|DialogDebuggerVisualizer Class<br /><br /> IDialogVisualizerService Interface|Data Object|  
|Object Provider (implements <xref:Microsoft.VisualStudio.DebuggerVisualizers.IVisualizerObjectProvider>)|Object Source (derived from <xref:Microsoft.VisualStudio.DebuggerVisualizers.VisualizerObjectSource>)|  
  
 The Object Provider provides the object data that is to be visualized to the visualizer UI. The Object Provider gets the object data from the Object Source. The Object Provider and Object Source provide APIs to communicate object data between the debugger side and the debugee side.  
  
 Every visualizer must get the data object to be visualized. The following table shows the corresponding APIs that the Object Provider and Object Source use for this purpose:  
  
|Object Provider|Object Source|  
|---------------------|-------------------|  
|<xref:Microsoft.VisualStudio.DebuggerVisualizers.IVisualizerObjectProvider.GetData*><br /><br /> —or—<br /><br /> <xref:Microsoft.VisualStudio.DebuggerVisualizers.IVisualizerObjectProvider.GetObject*>|<xref:Microsoft.VisualStudio.DebuggerVisualizers.VisualizerObjectSource.GetData*>|  
  
 Notice that the object provider can use either <xref:Microsoft.VisualStudio.DebuggerVisualizers.IVisualizerObjectProvider.GetData*> or <xref:Microsoft.VisualStudio.DebuggerVisualizers.IVisualizerObjectProvider.GetObject*>. Either API results in a call to <xref:Microsoft.VisualStudio.DebuggerVisualizers.VisualizerObjectSource.GetData*> on the Object Source. A call to <xref:Microsoft.VisualStudio.DebuggerVisualizers.VisualizerObjectSource.GetData*?displayProperty=fullName> fills in a [System.IO.Stream](assetId:///System.IO.Stream?qualifyHint=False&autoUpgrade=True), which represents a serialized form of the object that is being visualized.  
  
 <xref:Microsoft.VisualStudio.DebuggerVisualizers.IVisualizerObjectProvider.GetObject*?displayProperty=fullName> deserializes the data back into object form, which you can then display in the UI you create with <xref:Microsoft.VisualStudio.DebuggerVisualizers.DialogDebuggerVisualizer>. <xref:Microsoft.VisualStudio.DebuggerVisualizers.IVisualizerObjectProvider.GetData*?displayProperty=fullName> fills in the data as a raw assetId:///System.IO.Stream?qualifyHint=False&autoUpgrade=True, which you must deserialize yourself. <xref:Microsoft.VisualStudio.DebuggerVisualizers.IVisualizerObjectProvider.GetObject*?displayProperty=fullName> works by calling <xref:Microsoft.VisualStudio.DebuggerVisualizers.IVisualizerObjectProvider.GetData*?displayProperty=fullName> to get the serialized assetId:///System.IO.Stream?qualifyHint=False&autoUpgrade=True, then deserializing the data. Use <xref:Microsoft.VisualStudio.DebuggerVisualizers.IVisualizerObjectProvider.GetData*?displayProperty=fullName> when the object is not serializable by .NET and requires custom serialization. In that case, you must also override the <xref:Microsoft.VisualStudio.DebuggerVisualizers.VisualizerObjectSource.Serialize*?displayProperty=fullName> method.  
  
 If you are creating a read-only visualizer, one-way communication with <xref:Microsoft.VisualStudio.DebuggerVisualizers.IVisualizerObjectProvider.GetData*> or <xref:Microsoft.VisualStudio.DebuggerVisualizers.IVisualizerObjectProvider.GetObject*> is sufficient. If you are creating a visualizer that supports editing of data objects, you must do more. You must be able to send a data object from the Object Provider back to the Object Source also. The following table shows the Object Provider and Object Source APIs used for this purpose:  
  
|Object Provider|Object Source|  
|---------------------|-------------------|  
|<xref:Microsoft.VisualStudio.DebuggerVisualizers.IVisualizerObjectProvider.ReplaceData*><br /><br /> —or—<br /><br /> <xref:Microsoft.VisualStudio.DebuggerVisualizers.IVisualizerObjectProvider.ReplaceObject*>|<xref:Microsoft.VisualStudio.DebuggerVisualizers.VisualizerObjectSource.CreateReplacementObject*>|  
  
 Notice, again, that there are two APIs which the Object Provider can use. Data is always sent from the Object Provider to the Object Source as a assetId:///System.IO.Stream?qualifyHint=False&autoUpgrade=True, but <xref:Microsoft.VisualStudio.DebuggerVisualizers.IVisualizerObjectProvider.ReplaceData*> requires that you serialize the object into a assetId:///System.IO.Stream?qualifyHint=False&autoUpgrade=True yourself.  
  
 <xref:Microsoft.VisualStudio.DebuggerVisualizers.IVisualizerObjectProvider.ReplaceObject*> takes an object that you provide, serializes it into a assetId:///System.IO.Stream?qualifyHint=False&autoUpgrade=True, then calls <xref:Microsoft.VisualStudio.DebuggerVisualizers.IVisualizerObjectProvider.ReplaceData*> to send the assetId:///System.IO.Stream?qualifyHint=False&autoUpgrade=True to <xref:Microsoft.VisualStudio.DebuggerVisualizers.VisualizerObjectSource.CreateReplacementObject*>.  
  
 Using one of the Replace methods creates a new data object in the debuggee that replaces the object being visualized. If you want to change the contents of the original object without replacing it, use one of the Transfer methods shown in the following table. These APIs transfer data in both directions at the same time, without replacing the object that is being visualized:  
  
|Object Provider|Object Source|  
|---------------------|-------------------|  
|<xref:Microsoft.VisualStudio.DebuggerVisualizers.IVisualizerObjectProvider.TransferData*><br /><br /> —or—<br /><br /> <xref:Microsoft.VisualStudio.DebuggerVisualizers.IVisualizerObjectProvider.TransferObject*>|<xref:Microsoft.VisualStudio.DebuggerVisualizers.VisualizerObjectSource.TransferData*>|  
  
## See Also  
 [How to: Write a Visualizer](../debugger/how-to--write-a-visualizer.md)   
 [Walkthrough: Writing a Visualizer in C#](../debugger/walkthrough--writing-a-visualizer-in-csharp.md)   
 [Walkthrough: Writing a Visualizer in Visual Basic](../debugger/walkthrough--writing-a-visualizer-in-visual-basic.md)   
 [Walkthrough: Writing a Visualizer in Visual Basic](../debugger/walkthrough--writing-a-visualizer-in-visual-basic.md)   
 [Visualizer Security Considerations](../debugger/visualizer-security-considerations.md)