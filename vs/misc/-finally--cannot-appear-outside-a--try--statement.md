---
title: "&#39;Finally&#39; cannot appear outside a &#39;Try&#39; statement | hehe"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc30382"
  - "bc30382"
helpviewer_keywords: 
  - "BC30382"
ms.assetid: 0314d8d2-18bc-4bbd-858c-0a18408b52fd
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
# &#39;Finally&#39; cannot appear outside a &#39;Try&#39; statement
`Finally` is used to complete a `Try...Catch...Finally` block; hence it can only appear once at the end of the block. Either you have an unnecessary `Finally`, or your `Finally` statement appears outside the bounds of its corresponding `Try` block.  
  
 **Error ID:** BC30382  
  
### To correct this error  
  
1.  Locate and remove the unnecessary `Finally`statement.  
  
2.  Move the `Finally` statement to the appropriate location in your code.  
  
## See Also  
 [Try...Catch...Finally Statement](../Topic/Try...Catch...Finally%20Statement%20\(Visual%20Basic\).md)   
 [Structured Exception Handling Overview for Visual Basic](http://msdn.microsoft.com/en-us/bb81af80-a735-4873-9711-6151a48e418a)