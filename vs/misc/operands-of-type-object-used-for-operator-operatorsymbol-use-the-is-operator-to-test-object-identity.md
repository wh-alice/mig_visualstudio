---
title: "Operands of type Object used for operator &#39;&lt;operatorsymbol&gt;&#39;; use the &#39;Is&#39; operator to test object identity | Microsoft Docs"
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
  - "vbc42018"
  - "BC42018"
helpviewer_keywords: 
  - "BC42018"
ms.assetid: 3fc640a7-7dab-4c14-b25d-a5794dbba59d
caps.latest.revision: 12
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
# Operands of type Object used for operator &#39;&lt;operatorsymbol&gt;&#39;; use the &#39;Is&#39; operator to test object identity
An expression uses the `=` with one or both operands of the [Object Data Type](/dotnet/visual-basic/language-reference/data-types/object-data-type).  
  
 You should use the `Is` or `IsNot` operator to determine whether two object references refer to the same object instance. See "Comparing Objects" in [Comparison Operators in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/operators-and-expressions/comparison-operators).  
  
 When a variable or expression evaluates to `Object`, the compiler must perform *late binding*, which causes extra operations at run time. It also exposes your application to potential run-time errors. For example, if you assign a <xref:System.Windows.Forms.Form> to an `Object` variable and then try to use it with the `=` operator, the runtime throws an <xref:System.InvalidCastException> because Visual Basic cannot convert a <xref:System.Windows.Forms.Form> object to a data type suitable for value comparison. Even if both operands evaluate to type <xref:System.Windows.Forms.Form>, the operation fails because `=` is not defined for <xref:System.Windows.Forms.Form> operands.  
  
 By default, this message is a warning. For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../ide/configuring-warnings-in-visual-basic.md).  
  
 **Error ID:** BC42018  
  
### To correct this error  
  
-   If you want to determine whether two object references refer to the same object instance, use the `Is` or `IsNot` operator.  
  
## See Also  
 [Comparison Operators in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/operators-and-expressions/comparison-operators)   
 [Is Operator](/dotnet/visual-basic/language-reference/operators/is-operator)   
 [How to: Determine Whether Two Objects Are Related](http://msdn.microsoft.com/en-us/Library/da002e3f-6616-4bad-a229-f842d06652bb)   
 [How to: Determine Whether Two Objects Are Identical](http://msdn.microsoft.com/en-us/Library/7829f817-0d1f-4749-a707-de0b95e0cf5c)