---
title: "When Breakpoint Is Hit Dialog Box"
ms.custom: ""
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vs.debug.whenbreakpointishit"
dev_langs: 
  - "FSharp"
  - "VB"
  - "CSharp"
  - "C++"
  - "JScript"
  - "SQL"
  - "VB"
  - "CSharp"
  - "C++"
ms.assetid: 476e3d98-cf35-4338-b124-cd0f3010d854
caps.latest.revision: 11
ms.author: "mikejo"
manager: "ghogen"
translation.priority.ht: 
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "ru-ru"
  - "zh-cn"
  - "zh-tw"
translation.priority.mt: 
  - "cs-cz"
  - "pl-pl"
  - "pt-br"
  - "tr-tr"
---
# When Breakpoint Is Hit Dialog Box
With this dialog box, you can customize the action that occurs when a breakpoint is hit.  
  
## UIElement List  
 **Print a Message**  
 Prints a message, using DebuggerDisplay syntax. For more information, see [Using the DebuggerDisplay Attribute](../debugger/using-the-debuggerdisplay-attribute.md).  
  
 This textbox also supports special keywords (such as $ADDRESS) that can be used by themselves or within the curly braces of a DebuggerDisplay expression. The available keywords are listed on the dialog box.  
  
 **Continue Execution**  
 This control is enabled only when **Print a Message** is selected. With this control selected, you can use a breakpoint as a tracepoint to trace your program execution, rather than breaking when the location is hit.  
  
## See Also  
 [Using Breakpoints](../debugger/using-breakpoints.md)   
 [Using the DebuggerDisplay Attribute](../debugger/using-the-debuggerdisplay-attribute.md)