---
title: "Type &#39;&lt;typename&gt;&#39; must define operator &#39;&lt;determinantoperator&gt;&#39; to be used in a &#39;&lt;shortcircuitoperator&gt;&#39; expression | Microsoft Docs"
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
  - "bc33035"
  - "vbc33035"
helpviewer_keywords: 
  - "BC33035"
ms.assetid: 50a0a39f-63cd-4100-aea9-91b5b6ab5bbf
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
# Type &#39;&lt;typename&gt;&#39; must define operator &#39;&lt;determinantoperator&gt;&#39; to be used in a &#39;&lt;shortcircuitoperator&gt;&#39; expression
An [AndAlso Operator](/dotnet/visual-basic/language-reference/operators/andalso-operator) or an [OrElse Operator](/dotnet/visual-basic/language-reference/operators/orelse-operator) uses operands of a class or structure type, when that class or structure does not define a required operator.  
  
 Because you do not define a short-circuiting operator (`AndAlso` or `OrElse`) directly, you must define the corresponding logical and determinant operators. The following table shows the required operators.  
  
|Short-circuiting operator|Logical operator|Determinant operator|  
|--------------------------------|----------------------|--------------------------|  
|`AndAlso`|[And Operator](/dotnet/visual-basic/language-reference/operators/and-operator)|[IsFalse Operator](/dotnet/visual-basic/language-reference/operators/isfalse-operator)|  
|`OrElse`|[Or Operator](/dotnet/visual-basic/language-reference/operators/or-operator)|[IsTrue Operator](/dotnet/visual-basic/language-reference/operators/istrue-operator)|  
  
 [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] uses these logical and determinant operators to construct the short-circuiting logic for `AndAlso` or `OrElse`. For this to work properly, both operands and the return value of your `And` or `Or` definition must be of the containing type, that is, the type of the class or structure in which you are defining `And` or `Or`.  
  
 **Error ID:** BC33035  
  
### To correct this error  
  
-   Define the `And` and `IsFalse` operators, or the `Or` and `IsTrue` operators, in the class or structure used for the operand type of the `AndAlso` or `OrElse` operator. Be sure the operands for `And` or `Or` are of the type of the class or structure in which you define it.  
  
## See Also  
 [Operator Procedures](/dotnet/visual-basic/language-reference/procedures/operator-procedures)   
 [Operator Statement](/dotnet/visual-basic/language-reference/statements/operator-statement)   
 [How to: Define an Operator](http://msdn.microsoft.com/en-us/Library/d4b0e253-092a-4e6e-9fe2-01f562140a29)   
 [How to: Define a Conversion Operator](http://msdn.microsoft.com/en-us/Library/54203dfa-c24b-463f-9942-d5153e89e762)   
 [Logical and Bitwise Operators in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/operators-and-expressions/logical-and-bitwise-operators)