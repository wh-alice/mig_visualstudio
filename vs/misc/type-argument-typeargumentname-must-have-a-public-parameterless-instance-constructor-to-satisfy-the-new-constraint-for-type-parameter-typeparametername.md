---
title: "Type argument &#39;&lt;typeargumentname&gt;&#39; must have a public parameterless instance constructor to satisfy the &#39;New&#39; constraint for type parameter &#39;&lt;typeparametername&gt;&#39; | Microsoft Docs"
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
  - "vbc32083"
  - "BC32083"
helpviewer_keywords: 
  - "BC32083"
ms.assetid: 56bf25f1-375c-4b5d-9969-45eba8b3b66c
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
# Type argument &#39;&lt;typeargumentname&gt;&#39; must have a public parameterless instance constructor to satisfy the &#39;New&#39; constraint for type parameter &#39;&lt;typeparametername&gt;&#39;
A type argument supplies a type without an accessible parameterless constructor to a type parameter with the [New Operator](/dotnet/visual-basic/language-reference/operators/new-operator) constraint.  
  
 A constraint list imposes requirements on the type argument passed to the type parameter. One possible requirement is that the type argument must expose a parameterless constructor that the creating code can access. To specify this requirement, the constraint list includes the `New` constraint.  
  
 **Error ID:** BC32083  
  
### To correct this error  
  
1.  Verify that the generic type name and the type name in the type argument are spelled correctly.  
  
2.  Choose a type for the type argument that exposes an accessible parameterless constructor. You cannot invoke this particular generic type unless you can supply such a type argument to this type parameter.  
  
## See Also  
 [Generic Types in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-types)   
 [Type List](/dotnet/visual-basic/language-reference/statements/type-list)   
 [How to: Use a Generic Class](http://msdn.microsoft.com/en-us/Library/242dd2a6-86c4-4ce7-83f2-f2661803f752)