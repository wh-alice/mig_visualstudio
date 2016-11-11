---
title: "&#39;On Error&#39; statements are not valid within &#39;Using&#39; statements | Microsoft Docs"
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
  - "vbc36013"
  - "bc36013"
helpviewer_keywords: 
  - "BC36013"
ms.assetid: 5b399bf9-6595-46e0-a808-378f6c28568b
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
# &#39;On Error&#39; statements are not valid within &#39;Using&#39; statements
An `On Error` statement appears within a `Using` statement but is not valid in that context.  
  
 **Error ID:** BC36013  
  
### To correct this error  
  
-   Use structured error handling, such as a `Try…Catch` block, in place of the `On Error` statement.  
  
## See Also  
 [Structured Exception Handling Overview for Visual Basic](http://msdn.microsoft.com/en-us/bb81af80-a735-4873-9711-6151a48e418a)   
 [Choosing When to Use Structured and Unstructured Exception Handling (Visual Basic)](http://msdn.microsoft.com/en-us/e897d7ca-07e8-45dd-8a6d-a5b2a2fc9b9a)   
 [On Error Statement](/dotnet/visual-basic/language-reference/statements/on-error-statement)   
 [How to: Test Code with a Try…Catch Block in Visual Basic](http://msdn.microsoft.com/en-us/8368e205-ed73-4185-a247-af84fb4fafa9)   
 [Try...Catch...Finally Statement](/dotnet/visual-basic/language-reference/statements/try-catch-finally-statement)