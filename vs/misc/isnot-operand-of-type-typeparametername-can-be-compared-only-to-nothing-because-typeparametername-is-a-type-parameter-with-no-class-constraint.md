---
title: "&#39;IsNot&#39; operand of type &#39;&lt;typeparametername&gt;&#39; can be compared only to &#39;Nothing&#39; because &#39;&lt;typeparametername&gt;&#39; is a type parameter with no class constraint | Microsoft Docs"
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
  - "vbc32097"
  - "bc32097"
helpviewer_keywords: 
  - "BC32097"
ms.assetid: 50283a4b-70e3-4e59-9b9b-65e7cacf5ce1
caps.latest.revision: 11
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
# &#39;IsNot&#39; operand of type &#39;&lt;typeparametername&gt;&#39; can be compared only to &#39;Nothing&#39; because &#39;&lt;typeparametername&gt;&#39; is a type parameter with no class constraint
A type parameter is used as an operand for the [IsNot Operator](/dotnet/visual-basic/language-reference/operators/isnot-operator) when the type parameter is defined without either the [Class (Visual Basic)](http://msdn.microsoft.com/en-us/0777c6e6-46bc-451b-ad70-57b49d4ef4f7) keyword or a specific class name in its constraint list.  
  
 `IsNot` compares two reference types to determine whether they point to different object instances in memory. It cannot take an operand that is not a reference type unless the other operand is [Nothing](/dotnet/visual-basic/language-reference/nothing).  
  
 **Error ID:** BC32097  
  
### To correct this error  
  
-   If you can require that the type argument supplied to this type parameter always be a reference type, add either the `Class` keyword or a specific class name to the constraint list for the type parameter.  
  
-   If you cannot require that the type argument supplied to this type parameter always be a reference type, remove it from the `IsNot` expression. You cannot compare it to other reference types with the `IsNot` operator.  
  
## See Also  
 [Generic Types in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-types)   
 [Type List](/dotnet/visual-basic/language-reference/statements/type-list)   
 [Value Types and Reference Types](/dotnet/visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types)   
 [Comparison Operators in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/operators-and-expressions/comparison-operators)