---
title: "System.Diagnostics.DebuggerHiddenAttribute does not affect &#39;Get&#39; or &#39;Set&#39; when applied to the Property definition | Microsoft Docs"
ms.custom: ""
ms.date: "2015-07-20"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bc40051"
  - "vbc40051"
helpviewer_keywords: 
  - "BC40051"
ms.assetid: 623d5e48-7fb2-48a9-bbbb-92914b08c01c
caps.latest.revision: 10
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
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
# System.Diagnostics.DebuggerHiddenAttribute does not affect &#39;Get&#39; or &#39;Set&#39; when applied to the Property definition
System.Diagnostics.DebuggerHiddenAttribute does not affect 'Get' or 'Set' when applied to the Property definition. Apply the attribute directly to the 'Get' and 'Set' procedures as appropriate.  
  
 The <xref:System.Diagnostics.DebuggerHiddenAttribute> is applied to a property declaration.  
  
 Source code can apply the <xref:System.Diagnostics.DebuggerHiddenAttribute> to a procedure. Doing so signals the Visual Studio debugger not to stop inside the procedure and not to allow any breakpoints to be set in the procedure.  
  
 Although you can apply <xref:System.Diagnostics.DebuggerHiddenAttribute> to a property, it does not have any effect. It has the effect that you want only if you apply it to the property's `Get` or `Set` procedure.  
  
 By default, this message is a warning. For information about hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../ide/configuring-warnings-in-visual-basic.md).  
  
 **Error ID:** BC40051  
  
### To correct this error  
  
-   Remove the <xref:System.Diagnostics.DebuggerHiddenAttribute> from the property declaration and apply it to the property's `Get` or `Set` procedure as appropriate.  
  
## See Also  
 <xref:System.Diagnostics.DebuggerHiddenAttribute>   
 [Property Procedures](/dotnet/visual-basic/language-reference/procedures/property-procedures)   
 [Property Statement](/dotnet/visual-basic/language-reference/statements/property-statement)   
 [Get Statement](/dotnet/visual-basic/language-reference/statements/get-statement)   
 [Set Statement](/dotnet/visual-basic/language-reference/statements/set-statement)