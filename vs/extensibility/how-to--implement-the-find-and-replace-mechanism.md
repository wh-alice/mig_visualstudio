---
title: "How to: Implement the Find and Replace Mechanism"
ms.custom: ""
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "editors [Visual Studio SDK], legacy - find and replace"
ms.assetid: bbd348db-3d19-42eb-99a2-3e808528c0ca
caps.latest.revision: 11
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
# How to: Implement the Find and Replace Mechanism
Visual Studio provides two ways of implementing Find/Replace. One way is to pass a text image to the shell and let it handle searching, highlighting, and replacing text. This allows users to specify multiple text spans. Alternatively, your VSPackage can control this functionality itself. In both cases you must notify the shell about the current target and the targets for all open documents.  
  
### To implement Find/Replace  
  
1.  Implement the <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget> interface on one of the objects returned by the frame properties <xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID> or <xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID>. If you are creating a custom editor, you should implement this interface as part of the custom editor class.  
  
2.  Use the <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.GetCapabilities*> method to specify the options that your editor supports and to indicate whether it implements text image searching.  
  
     If your editor supports text image searching, implement <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.GetSearchImage*>.  
  
     Otherwise, implement <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Find*> and <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Replace*>.  
  
3.  If you implement the <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Find*> and <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Replace*> methods, you can simplify your searching tasks by calling the <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindHelper> interface.  
  
## See Also  
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindHelper>   
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget>   
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Find*>   
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.GetSearchImage*>   
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Replace*>   
 <xref:Microsoft.VisualStudio.Shell.Interop.__VSPROPID>