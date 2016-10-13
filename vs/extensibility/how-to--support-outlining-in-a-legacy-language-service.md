---
title: "How to: Support Outlining in a Legacy Language Service"
ms.custom: na
ms.date: "10/06/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "editors [Visual Studio SDK], collapse to definitions command"
  - "language services, supporting Collapse to Definitions command"
  - "hidden text, Collapse to Definitions command"
ms.assetid: bb6e74c3-93e4-4ef7-afc7-1c9b342f083b
caps.latest.revision: 17
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
# How to: Support Outlining in a Legacy Language Service
Outlining is used to expand or collapse different regions of text. The way outlining is used can be defined differently by different languages. For more information, see [Outlining](../ide/outlining.md).  
  
 Legacy language services are implemented as part of a VSPackage, but the newer way to implement language service features is to use MEF extensions. To find out more about the new way to implement outlining, see [Walkthrough: Outlining](../extensibility/walkthrough--outlining.md).  
  
> [!NOTE]
>  We recommend that you begin to use the new editor API as soon as possible. This will improve the performance of your language service and let you take advantage of new editor features.  
  
 The following demonstrates how to support this command for your language service.  
  
### To support outlining  
  
1.  Implement \<xref:Microsoft.VisualStudio.TextManager.Interop.IVsOutliningCapableLanguage> on your language service object.  
  
2.  Call \<xref:Microsoft.VisualStudio.TextManager.Interop.IVsOutliningSession.AddOutlineRegions*> on the current outlining session object to add new outline regions.  
  
## Robust Programming  
 When a user selects **Collapse To Definitions** on the **Outlining** menu, the IDE calls \<xref:Microsoft.VisualStudio.TextManager.Interop.IVsOutliningCapableLanguage.CollapseToDefinitions*> on your language service.  
  
 When this method is called, the IDE passes in an \<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLines> pointer (a pointer to a text buffer) and an \<xref:Microsoft.VisualStudio.TextManager.Interop.IVsOutliningSession> (a pointer to the current outlining session).  
  
 You can call the \<xref:Microsoft.VisualStudio.TextManager.Interop.IVsOutliningSession.AddOutlineRegions*> method for multiple outline regions by specifying these regions in the `rgOutlnReg` parameter. The `rgOutlnReg` parameter is a \<xref:Microsoft.VisualStudio.TextManager.Interop.NewOutlineRegion> structure. This process lets you to specify different characteristics of the hidden region, such as whether a particular region is expanded or collapsed.  
  
> [!NOTE]
>  Be careful about hiding new-line characters. Hidden text should extend from the start of the first line to the last character of the last line in a section, leaving the final new-line character visible.  
  
## See Also  
 [How to: Provide Hidden Text Support in a Legacy Language Service](../extensibility/how-to--provide-hidden-text-support-in-a-legacy-language-service.md)   
 [How to: Provide Expanded Outlining Support in a Legacy Language Service](../extensibility/how-to--provide-expanded-outlining-support-in-a-legacy-language-service.md)