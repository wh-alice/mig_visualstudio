---
title: "Operator &#39;&lt;operator&gt;&#39; must have a return type of Boolean | Microsoft Docs"
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
  - "vbc33023"
  - "bc33023"
helpviewer_keywords: 
  - "BC33023"
ms.assetid: 18e066f4-d71e-4e38-b0bc-8af9145f6015
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
# Operator &#39;&lt;operator&gt;&#39; must have a return type of Boolean
A comparison or logical operator is declared with a return type other than the [Boolean Data Type](/dotnet/visual-basic/language-reference/data-types/boolean-data-type).  
  
 The result of a comparison operator (`=`, `<>`, `<`, `<=`, `>`, `>=`, `Is`, `IsNot`, `IsFalse`, `IsTrue`, `Like`, `TypeOf`) can be only `True` or `False`. For more information, see [Comparison Operators in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/operators-and-expressions/comparison-operators).  
  
 Logical operators (`And`, `AndAlso`, `Not`, `Or`, `OrElse`, `Xor`) work entirely within the domain of Boolean values. For more information, see [Logical and Bitwise Operators in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/operators-and-expressions/logical-and-bitwise-operators).  
  
 **Error ID:** BC33023  
  
### To correct this error  
  
-   Replace the return type of this comparison or logical operator with `Boolean`.  
  
## See Also  
 [Operator Procedures](/dotnet/visual-basic/language-reference/procedures/operator-procedures)   
 [Operator Statement](/dotnet/visual-basic/language-reference/statements/operator-statement)   
 [How to: Define an Operator](../Topic/How%20to:%20Define%20an%20Operator%20\(Visual%20Basic\).md)   
 [How to: Define a Conversion Operator](../Topic/How%20to:%20Define%20a%20Conversion%20Operator%20\(Visual%20Basic\).md)