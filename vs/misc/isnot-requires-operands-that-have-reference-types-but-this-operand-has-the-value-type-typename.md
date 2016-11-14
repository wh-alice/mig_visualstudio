---
title: "&#39;IsNot&#39; requires operands that have reference types, but this operand has the value type &#39;&lt;typename&gt;&#39;. | Microsoft Docs"
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
  - "bc31419"
  - "vbc31419"
helpviewer_keywords: 
  - "BC31419"
ms.assetid: c44d2936-8c07-443a-b320-ac2bfbc1e9ec
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
# &#39;IsNot&#39; requires operands that have reference types, but this operand has the value type &#39;&lt;typename&gt;&#39;.
An expression uses the [IsNot Operator](/dotnet/visual-basic/language-reference/operators/isnot-operator) with at least one value type operand.  
  
 The `IsNot` operator determines whether two object references refer to different objects. It compares the pointer values of reference types and is meaningless with value types.  
  
 **Error ID:** BC31419  
  
### To correct this error  
  
-   If you intend to compare the values of two value types, use the `=` or `<>` comparison operator.  
  
-   If you intend to compare the pointers of two reference types, be sure you are using object references for both operands. You can use reference variables or elements, such as the [Me](http://msdn.microsoft.com/en-us/a65973c7-cf06-4547-9b25-9fba885525c2) keyword, that behave like reference variables.  
  
## See Also  
 [Comparison Operators in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/operators-and-expressions/comparison-operators)   
 [How to: Test Whether Two Objects Are the Same](http://msdn.microsoft.com/en-us/Library/f760e828-8704-4256-bc2d-c22a4c93b524)