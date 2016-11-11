---
title: "Option Strict On disallows implicit conversions from &#39;&lt;type1&gt;&#39; to &#39;&lt;type2&gt;&#39; | Microsoft Docs"
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
  - "bc30512"
  - "vbc30512"
helpviewer_keywords: 
  - "BC30512"
ms.assetid: b9756d48-05fa-4027-8a80-b4a0ef92099d
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
# Option Strict On disallows implicit conversions from &#39;&lt;type1&gt;&#39; to &#39;&lt;type2&gt;&#39;
You have tried to convert a type to another type that may not be able to contain the value, such as a `Long` to an `Integer`, while the type checking switch ([Option Strict Statement](/dotnet/visual-basic/language-reference/statements/option-strict-statement)) is set to `On`.  
  
 This type of conversion is called a *narrowing conversion*, and it is possible for it to fail at run time. For this reason, `Option Strict On` disallows implicit narrowing conversions.  
  
 **Error ID:** BC30512  
  
### To correct this error  
  
1.  Determine whether a conversion of any type exists from `<type1>` to `<type2>`. If both are [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] elementary types, or if both are instances of classes, you can usually make this determination by consulting the table in [Widening and Narrowing Conversions](/dotnet/visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions).  
  
2.  If only a narrowing conversion exists from `<type1>` to `<type2>`, you should use explicit casting. The [CType Function](/dotnet/visual-basic/language-reference/functions/ctype-function) and [DirectCast Operator](/dotnet/visual-basic/language-reference/operators/directcast-operator) keywords throw a run-time exception if the conversion fails. The [TryCast Operator](/dotnet/visual-basic/language-reference/operators/trycast-operator) keyword applies only to reference types and returns [Nothing](/dotnet/visual-basic/language-reference/nothing) if the conversion fails.  
  
3.  If a narrowing conversion exists and your program can tolerate a run-time failure, or you are confident that a run-time failure is not possible, you can specify `Option Strict Off` at the beginning of your source code. But you should still enclose the conversion in a [Try...Catch...Finally Statement](/dotnet/visual-basic/language-reference/statements/try-catch-finally-statement) block to avoid unexpected results or early termination of your program.  
  
4.  If no conversion exists from `<type1>` to `<type2>`, you must re-evaluate your program logic. You might be able to write code that can assign values to `<type2>` corresponding to anticipated values of `<type1>`.  
  
5.  If no conversion exists from `<type1>` to `<type2>` and one of the types is a class or structure you have defined, you might be able to define a conversion operator from that type to or from the other type. For more information, see [How to: Define a Conversion Operator](../Topic/How%20to:%20Define%20a%20Conversion%20Operator%20\(Visual%20Basic\).md).  
  
6.  In all cases and as a general guideline, you should avoid using narrowing conversions unless you can trap failures in a `Catch` block and deal with them effectively.  
  
## See Also  
 [Option Strict Statement](/dotnet/visual-basic/language-reference/statements/option-strict-statement)   
 [Widening and Narrowing Conversions](/dotnet/visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions)   
 [CType Function](/dotnet/visual-basic/language-reference/functions/ctype-function)   
 [DirectCast Operator](/dotnet/visual-basic/language-reference/operators/directcast-operator)   
 [TryCast Operator](/dotnet/visual-basic/language-reference/operators/trycast-operator)   
 [Nothing](/dotnet/visual-basic/language-reference/nothing)   
 [Try...Catch...Finally Statement](/dotnet/visual-basic/language-reference/statements/try-catch-finally-statement)   
 [How to: Define a Conversion Operator](../Topic/How%20to:%20Define%20a%20Conversion%20Operator%20\(Visual%20Basic\).md)