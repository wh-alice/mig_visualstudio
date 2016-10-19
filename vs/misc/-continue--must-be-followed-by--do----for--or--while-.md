---
title: "&#39;Continue&#39; must be followed by &#39;Do&#39;, &#39;For&#39; or &#39;While&#39;"
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
  - "bc30781"
  - "vbc30781"
helpviewer_keywords: 
  - "BC30781"
ms.assetid: a0d5854d-ca44-4c6b-9458-4fc50d29281a
caps.latest.revision: 9
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
# &#39;Continue&#39; must be followed by &#39;Do&#39;, &#39;For&#39; or &#39;While&#39;
A `Continue` statement must be followed by `Do`, `For`, or `While`, depending on if the `Continue` statement appears within a `Do...Loop` loop, `For...Next` loop, or `While...End While` loop.  
  
 **Error ID:** BC30781  
  
### To correct this error  
  
1.  If the `Continue` statement is in a `Do...Loop` loop, change the statement to `Continue Do`.  
  
2.  If the `Continue` statement is in a `For...Next` loop, change the statement to `Continue For`.  
  
3.  If the `Continue` statement is in a `While...End While` loop, change the statement to `Continue While`.  
  
4.  Otherwise, remove the `Continue` statement.  
  
## See Also  
 [Continue Statement](../Topic/Continue%20Statement%20\(Visual%20Basic\).md)