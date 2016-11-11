---
title: "Relational operator expected | Microsoft Docs"
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
  - "bc30239"
  - "vbc30239"
helpviewer_keywords: 
  - "BC30239"
ms.assetid: c5701568-77a1-441b-a0f7-f7b36cbd17e3
caps.latest.revision: 8
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
# Relational operator expected
A `Case` statement contains an `Is` clause but no comparison operator such as `=` or `>`. If a `Case` statement does not include an operator, `=` is assumed and `Is` is not used.  
  
 **Error ID:** BC30239  
  
### To correct this error  
  
-   Remove the `Is` keyword or follow it with a comparison operator.  
  
## See Also  
 [Select...Case Statement](/dotnet/visual-basic/language-reference/statements/select-case-statement)   
 [Comparison Operators in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/operators-and-expressions/comparison-operators)   
 [Comparison Operators](/dotnet/visual-basic/language-reference/operators/comparison-operators)