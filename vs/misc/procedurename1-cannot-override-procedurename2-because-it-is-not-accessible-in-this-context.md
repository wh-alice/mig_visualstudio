---
title: "&#39;&lt;procedurename1&gt;&#39; cannot override &#39;&lt;procedurename2&gt;&#39; because it is not accessible in this context | Microsoft Docs"
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
  - "bc31417"
  - "vbc31417"
helpviewer_keywords: 
  - "BC31417"
ms.assetid: 1a36acbf-cead-43a0-b12f-f52f94d09124
caps.latest.revision: 9
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
# &#39;&lt;procedurename1&gt;&#39; cannot override &#39;&lt;procedurename2&gt;&#39; because it is not accessible in this context
A procedure or property overrides a procedure or property with an access level that prevents access by the overriding procedure or property.  
  
 For example, if a procedure is declared as `Friend` in one assembly, it cannot be accessed outside that assembly. If a procedure in another assembly in the same project attempts to override the `Friend` procedure, it cannot access it to override it.  
  
 **Error ID:** BC31417  
  
### To correct this error  
  
-   Move the overriding procedure or property to the same assembly as the procedure or property it is to override.  
  
     -or-  
  
-   Remove the `Overrides` keyword.  
  
## See Also  
 [Access Levels in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/declared-elements/access-levels)   
 [Overrides](/dotnet/visual-basic/language-reference/modifiers/overrides)   
 [NOT IN BUILD: Overriding Properties and Methods](http://msdn.microsoft.com/en-us/2167e8f5-1225-4b13-9ebd-02591ba90213)