---
title: "&#39;End Try&#39; must be preceded by a matching &#39;Try&#39;"
ms.custom: ""
ms.date: "10/13/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bc30383"
  - "vbc30383"
helpviewer_keywords: 
  - "BC30383"
ms.assetid: 1d13357a-ab44-4082-b204-6e2e94f4774e
caps.latest.revision: 7
ms.author: "billchi"
manager: "douge"
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
# &#39;End Try&#39; must be preceded by a matching &#39;Try&#39;
`End` `Try` is used to complete a `Try` block, and hence it can only appear at the end of the block. Either you have a redundant `End Try` statement, or your `End``Try` statement appears outside the bounds of its corresponding `Try` block.  
  
 **Error ID:** BC30383  
  
### To correct this error  
  
1.  Locate and remove the unnecessary `End Try`.  
  
2.  Move the `End Try` to the appropriate location in your code.  
  
## See Also  
 [Try...Catch...Finally Statement](../Topic/Try...Catch...Finally%20Statement%20\(Visual%20Basic\).md)   
 [Structured Exception Handling Overview for Visual Basic](http://msdn.microsoft.com/en-us/bb81af80-a735-4873-9711-6151a48e418a)