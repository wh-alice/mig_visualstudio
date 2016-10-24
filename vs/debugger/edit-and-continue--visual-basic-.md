---
title: "Edit and Continue (Visual Basic) | testtitle"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "FSharp"
  - "VB"
  - "CSharp"
  - "C++"
  - "VB"
helpviewer_keywords: 
  - "Edit and Continue, 64-bit"
  - "Edit and Continue [Visual Basic]"
  - "debugging [Visual Basic], Edit and Continue"
  - "Visual Basic, Edit and Continue"
  - "64-bit Edit and Continue"
ms.assetid: 7e90f34f-e699-45ab-a4c9-a4b527c498c8
caps.latest.revision: 40
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
# Edit and Continue (Visual Basic)
Edit and Continue is a feature for [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] debugging that enables you to change your code while it is executing in Break mode. After code edits have been applied, you can resume code execution with the new edits in place and see the effect.  
  
 You can use the Edit and Continue feature whenever you enter Break mode. In Break mode, the instruction pointer, a yellow arrowhead in the source window, points to the line that will be executed next, and will be located on an executable statement within a method or property body. You can make almost any kind of change to executable statements while in Break mode, and the change will be incorporated into the underlying project. While in Break mode, however, you are generally not allowed to change declaration statements, such as public methods, public fields, or class declarations.  
  
 When you make an unauthorized edit, the change is marked with a purple wavy underline and a task is displayed in the Task List. You must undo an unauthorized edit if you want to continue to use Edit and Continue. Certain unauthorized edits may be permitted if done outside Edit and Continue. If you want to retain the results of such an unauthorized edit, you must stop debugging and restart your application.  
  
 Edit and Continue is supported for 64-bit projects that target the .NET Framework 4.5.1.  
  
 Edit and Continue is not supported when you start debugging using **Attach to Process**. Edit and Continue is not supported for optimized code, mixed managed and native code, or Compact Framework (Smart Device) projects.  
  
 The topics in this section provide additional details about how to use this feature and what kinds of changes are not allowed.  
  
## In This Section  
 [How to: Apply Edits in Break Mode with Edit and Continue](../debugger/how-to--apply-edits-in-break-mode-with-edit-and-continue.md)  
 Explains how to apply code edits in Break mode.  
  
 [Unsupported Edits in Visual Basic Edit and Continue](../debugger/unsupported-edits-in-visual-basic-edit-and-continue.md)  
 Describes what types of edits cannot be performed in [!INCLUDE[vb_current_short](../code-quality/includes/vb_current_short_md.md)] Edit and Continue.  
  
## Related Sections  
 [Edit and Continue](../debugger/edit-and-continue.md)  
 Provides a list of topics on Edit and Continue.