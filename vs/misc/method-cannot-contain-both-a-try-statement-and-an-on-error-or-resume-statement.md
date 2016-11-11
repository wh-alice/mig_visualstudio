---
title: "Method cannot contain both a &#39;Try&#39; statement and an &#39;On Error&#39; or &#39;Resume&#39; statement | Microsoft Docs"
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
  - "vbc30544"
  - "bc30544"
helpviewer_keywords: 
  - "BC30544"
ms.assetid: 1e75d5fe-9a6b-43c2-9749-1f2d7ce5b10d
caps.latest.revision: 7
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
# Method cannot contain both a &#39;Try&#39; statement and an &#39;On Error&#39; or &#39;Resume&#39; statement
You have combined a `Try` statement with `On Error` or `Resume`.  
  
 **Error ID:** BC30544  
  
### To correct this error  
  
1.  Remove the `On Error` or `Resume`.  
  
## See Also  
 [Structured Exception Handling Overview for Visual Basic](http://msdn.microsoft.com/en-us/bb81af80-a735-4873-9711-6151a48e418a)   
 [Try...Catch...Finally Statement](/dotnet/visual-basic/language-reference/statements/try-catch-finally-statement)