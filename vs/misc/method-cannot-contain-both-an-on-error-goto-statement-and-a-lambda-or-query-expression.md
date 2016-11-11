---
title: "Method cannot contain both an &#39;On Error GoTo&#39; statement and a lambda or query expression | Microsoft Docs"
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
  - "bc36595"
  - "vbc36595"
helpviewer_keywords: 
  - "BC36595"
ms.assetid: 4e7cc11e-f53d-4481-afb4-653a81d54483
caps.latest.revision: 4
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
# Method cannot contain both an &#39;On Error GoTo&#39; statement and a lambda or query expression
A method contains both an `On Error Goto` statement and either a lambda expression or a LINQ query. You cannot include an `On Error Goto` statement with a lambda expression or LINQ query in a method.  
  
 **Error ID:** BC36595  
  
### To correct this error  
  
1.  Replace the exception handling code that uses the `On Error Goto` statement with a `Try...Catch` statement.  
  
## See Also  
 [Introduction to Exception Handling (Visual Basic)](http://msdn.microsoft.com/en-us/9792f16a-0cd2-40bd-ace2-f7a4344c0e52)   
 [Try...Catch...Finally Statement](/dotnet/visual-basic/language-reference/statements/try-catch-finally-statement)   
 [Introduction to LINQ in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/linq/introduction-to-linq)   
 [Lambda Expressions](/dotnet/visual-basic/language-reference/procedures/lambda-expressions)   
 [On Error Statement](/dotnet/visual-basic/language-reference/statements/on-error-statement)