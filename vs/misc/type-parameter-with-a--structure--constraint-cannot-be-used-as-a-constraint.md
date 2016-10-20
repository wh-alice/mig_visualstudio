---
title: "Type parameter with a &#39;Structure&#39; constraint cannot be used as a constraint | Microsoft Docs"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc32114"
  - "bc32114"
helpviewer_keywords: 
  - "BC32114"
ms.assetid: 442b2048-9dc4-4223-bcfc-4d96bf8d14de
caps.latest.revision: 8
ms.author: "billchi"
manager: "douge"
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
# Type parameter with a &#39;Structure&#39; constraint cannot be used as a constraint
A type parameter with a `Structure` constraint is used as the constraint for another type parameter.  
  
 The `Structure` constraint requires that the type argument passed to its type parameter be a value type. However, a value type cannot be implemented or inherited, so it is not meaningful to use it as a constraint, which would require the other type parameter to implement it or inherit from it.  
  
 The only meaningful interpretation of this situation is that both type arguments must be of the exact same type. If that is the case, your generic type needs only one type parameter.  
  
 The following statement can generate this error.  
  
 `Class c1(Of t1 As Structure, t2 As t1)`  
  
 The type passed to `t2` cannot implement or inherit the type passed to `t1`, because the type passed to `t1` must be a value type.  
  
 **Error ID:** BC32114  
  
### To correct this error  
  
-   Remove the type parameter constrained to `Structure` from the constraint list on the other type parameter.  
  
-   If both type parameters require the same value type, define the generic type with only one type parameter.  
  
## See Also  
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Type List](../Topic/Type%20List%20\(Visual%20Basic\).md)   
 [Structure (Visual Basic)](http://msdn.microsoft.com/en-us/263ce115-ac36-4c05-8cb7-0e0eead5c6d0)   
 [Value Types and Reference Types](../Topic/Value%20Types%20and%20Reference%20Types.md)