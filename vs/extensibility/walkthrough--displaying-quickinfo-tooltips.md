---
title: "Walkthrough: Displaying QuickInfo Tooltips | Microsoft Docs"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "editors [Visual Studio SDK], new - QuickInfo"
ms.assetid: 23fb8384-4f12-446f-977f-ce7910347947
caps.latest.revision: 27
ms.author: "gregvanl"
manager: "ghogen"
translation.priority.mt: 
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
# Walkthrough: Displaying QuickInfo Tooltips
QuickInfo is an IntelliSense feature that displays method signatures and descriptions when a user moves the pointer over a method name. You can implement language-based features such as QuickInfo by defining the identifiers for which you want to provide QuickInfo descriptions, and then creating a tooltip in which to display the content. You can define QuickInfo in the context of a language service, or you can define your own file name extension and content type and display the QuickInfo for just that type, or you can display QuickInfo for an existing content type (such as "text"). This walkthrough shows how to display QuickInfo for the "text" content type.  
  
 The QuickInfo example in this walkthrough displays the tooltips when a user moves the pointer over a method name. This design requires you to implement these four interfaces:  
  
-   source interface  
  
-   source provider interface  
  
-   controller interface  
  
-   controller provider interface  
  
 The source and controller providers are Managed Extensibility Framework (MEF) component parts, and are responsible for exporting the source and controller classes and importing services and brokers such as the <xref:Microsoft.VisualStudio.Text.ITextBufferFactoryService>, which creates the tooltip text buffer, and the <xref:Microsoft.VisualStudio.Language.Intellisense.IQuickInfoBroker>, which triggers the QuickInfo session.  
  
 In this example, the QuickInfo source uses a hard-coded list of method names and descriptions, but in full implementations, the language service and the language documentation are responsible for providing that content.  
  
## Prerequisites  
 Starting in Visual Studio 2015, you do not install the Visual Studio SDK from the download center. It is included as an optional feature in Visual Studio setup. You can also install the VS SDK later on. For more information, see [Installing the Visual Studio SDK](../extensibility/installing-the-visual-studio-sdk.md).  
  
## Creating a MEF Project  
  
#### To create a MEF project  
  
1.  Create a C# VSIX project. (In the **New Project** dialog, select **Visual C# / Extensibility**, then **VSIX Project**.) Name the solution `QuickInfoTest`.  
  
2.  Add an Editor Classifier item template to the project. For more information, see [Creating an Extension with an Editor Item Template](../extensibility/creating-an-extension-with-an-editor-item-template.md).  
  
3.  Delete the existing class files.  
  
## Implementing the QuickInfo Source  
 The QuickInfo source is responsible for collecting the set of identifiers and their descriptions and adding the content to the tooltip text buffer when one of the identifiers is encountered. In this example, the identifiers and their descriptions are just added in the source constructor.  
  
#### To implement the QuickInfo source  
  
1.  Add a class file and name it `TestQuickInfoSource`.  
  
2.  Add a reference to Microsoft.VisualStudio.Language.IntelliSense.  
  
3.  Add the following imports.  
  
     [!CODE [VSSDKQuickInfoTest#1](../CodeSnippet/VS_Snippets_VSSDK/vssdkquickinfotest#1)]  
  
4.  Declare a class that implements <xref:Microsoft.VisualStudio.Language.Intellisense.IQuickInfoSource>, and name it `TestQuickInfoSource`.  
  
     [!CODE [VSSDKQuickInfoTest#2](../CodeSnippet/VS_Snippets_VSSDK/vssdkquickinfotest#2)]  
  
5.  Add fields for the QuickInfo source provider, the text buffer, and a set of method names and method signatures. In this example, the method names and signatures are initialized in the `TestQuickInfoSource` constructor.  
  
     [!CODE [VSSDKQuickInfoTest#3](../CodeSnippet/VS_Snippets_VSSDK/vssdkquickinfotest#3)]  
  
6.  Add a constructor that sets the QuickInfo source provider and the text buffer, and populates the set of method names, and method signatures and descriptions.  
  
     [!CODE [VSSDKQuickInfoTest#4](../CodeSnippet/VS_Snippets_VSSDK/vssdkquickinfotest#4)]  
  
7.  Implement the <xref:Microsoft.VisualStudio.Language.Intellisense.IQuickInfoSource.AugmentQuickInfoSession*> method. In this example, the method finds the current word, or the previous word if the cursor is at the end of a line or a text buffer. If the word is one of the method names, the description for that method name is added to the QuickInfo content.  
  
     [!CODE [VSSDKQuickInfoTest#5](../CodeSnippet/VS_Snippets_VSSDK/vssdkquickinfotest#5)]  
  
8.  You must also implement a Dispose() method, since <xref:Microsoft.VisualStudio.Language.Intellisense.IQuickInfoSource> implements <xref:System.IDisposable>:  
  
     [!CODE [VSSDKQuickInfoTest#6](../CodeSnippet/VS_Snippets_VSSDK/vssdkquickinfotest#6)]  
  
## Implementing a QuickInfo Source Provider  
 The provider of the QuickInfo source serves primarily to export itself as a MEF component part and instantiate the QuickInfo source. Because it is a MEF component part, it can import other MEF component parts.  
  
#### To implement a QuickInfo source provider  
  
1.  Declare a QuickInfo source provider named `TestQuickInfoSourceProvider` that implements <xref:Microsoft.VisualStudio.Language.Intellisense.IQuickInfoSourceProvider>, and export it with a <xref:Microsoft.VisualStudio.Utilities.NameAttribute> of "ToolTip QuickInfo Source", an <xref:Microsoft.VisualStudio.Utilities.OrderAttribute> of Before="default", and a <xref:Microsoft.VisualStudio.Utilities.ContentTypeAttribute> of "text".  
  
     [!CODE [VSSDKQuickInfoTest#7](../CodeSnippet/VS_Snippets_VSSDK/vssdkquickinfotest#7)]  
  
2.  Import two editor services, <xref:Microsoft.VisualStudio.Text.Operations.ITextStructureNavigatorSelectorService> and <xref:Microsoft.VisualStudio.Text.ITextBufferFactoryService>, as properties of `TestQuickInfoSourceProvider`.  
  
     [!CODE [VSSDKQuickInfoTest#8](../CodeSnippet/VS_Snippets_VSSDK/vssdkquickinfotest#8)]  
  
3.  Implement <xref:Microsoft.VisualStudio.Language.Intellisense.IQuickInfoSourceProvider.TryCreateQuickInfoSource*> to return a new `TestQuickInfoSource`.  
  
     [!CODE [VSSDKQuickInfoTest#9](../CodeSnippet/VS_Snippets_VSSDK/vssdkquickinfotest#9)]  
  
## Implementing a QuickInfo Controller  
 QuickInfo controllers determine when QuickInfo should be displayed. In this example, QuickInfo is displayed when the pointer is over a word that corresponds to one of the method names. The QuickInfo controller implements a mouse hover event handler that triggers a QuickInfo session.  
  
#### To implement a QuickInfo controller  
  
1.  Declare a class that implements <xref:Microsoft.VisualStudio.Language.Intellisense.IIntellisenseController>, and name it `TestQuickInfoController`.  
  
     [!CODE [VSSDKQuickInfoTest#10](../CodeSnippet/VS_Snippets_VSSDK/vssdkquickinfotest#10)]  
  
2.  Add private fields for the text view, the text buffers represented in the text view, the QuickInfo session, and the QuickInfo controller provider.  
  
     [!CODE [VSSDKQuickInfoTest#11](../CodeSnippet/VS_Snippets_VSSDK/vssdkquickinfotest#11)]  
  
3.  Add a constructor that sets the fields and adds the mouse hover event handler.  
  
     [!CODE [VSSDKQuickInfoTest#12](../CodeSnippet/VS_Snippets_VSSDK/vssdkquickinfotest#12)]  
  
4.  Add the mouse hover event handler that triggers the QuickInfo session.  
  
     [!CODE [VSSDKQuickInfoTest#13](../CodeSnippet/VS_Snippets_VSSDK/vssdkquickinfotest#13)]  
  
5.  Implement the <xref:Microsoft.VisualStudio.Language.Intellisense.IIntellisenseController.Detach*> method so that it removes the mouse hover event handler when the controller is detached from the text view.  
  
     [!CODE [VSSDKQuickInfoTest#14](../CodeSnippet/VS_Snippets_VSSDK/vssdkquickinfotest#14)]  
  
6.  Implement the <xref:Microsoft.VisualStudio.Language.Intellisense.IIntellisenseController.ConnectSubjectBuffer*> method and the <xref:Microsoft.VisualStudio.Language.Intellisense.IIntellisenseController.DisconnectSubjectBuffer*> method as empty methods for this example.  
  
     [!CODE [VSSDKQuickInfoTest#15](../CodeSnippet/VS_Snippets_VSSDK/vssdkquickinfotest#15)]  
  
## Implementing the QuickInfo Controller Provider  
 The provider of the QuickInfo controller serves primarily to export itself as a MEF component part and instantiate the QuickInfo controller. Because it is a MEF component part, it can import other MEF component parts.  
  
#### To implement the QuickInfo controller provider  
  
1.  Declare a class named `TestQuickInfoControllerProvider` that implements <xref:Microsoft.VisualStudio.Language.Intellisense.IIntellisenseControllerProvider>, and export it with a <xref:Microsoft.VisualStudio.Utilities.NameAttribute> of "ToolTip QuickInfo Controller" and a <xref:Microsoft.VisualStudio.Utilities.ContentTypeAttribute> of "text":  
  
     [!CODE [VSSDKQuickInfoTest#16](../CodeSnippet/VS_Snippets_VSSDK/vssdkquickinfotest#16)]  
  
2.  Import the <xref:Microsoft.VisualStudio.Language.Intellisense.IQuickInfoBroker> as a property.  
  
     [!CODE [VSSDKQuickInfoTest#17](../CodeSnippet/VS_Snippets_VSSDK/vssdkquickinfotest#17)]  
  
3.  Implement the <xref:Microsoft.VisualStudio.Language.Intellisense.IIntellisenseControllerProvider.TryCreateIntellisenseController*> method by instantiating the QuickInfo controller.  
  
     [!CODE [VSSDKQuickInfoTest#18](../CodeSnippet/VS_Snippets_VSSDK/vssdkquickinfotest#18)]  
  
## Building and Testing the Code  
 To test this code, build the QuickInfoTest solution and run it in the experimental instance.  
  
#### To build and test the QuickInfoTest solution  
  
1.  Build the solution.  
  
2.  When you run this project in the debugger, a second instance of Visual Studio is instantiated.  
  
3.  Create a text file and type some text that includes the words "add" and "subtract".  
  
4.  Move the pointer over one of the occurrences of "add". The signature and the description of the `add` method should be displayed.  
  
## See Also  
 [Walkthrough: Linking a Content Type to a File Name Extension](../extensibility/walkthrough--linking-a-content-type-to-a-file-name-extension.md)