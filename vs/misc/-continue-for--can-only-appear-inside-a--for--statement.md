---
title: "&#39;Continue For&#39; can only appear inside a &#39;For&#39; statement"
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
  - "bc30783"
  - "vbc30783"
helpviewer_keywords: 
  - "BC30783"
ms.assetid: 70891018-27c8-4d36-b168-8cc7177d70cb
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
# &#39;Continue For&#39; can only appear inside a &#39;For&#39; statement
A `Continue For` statement can only appear within a `For...Next` loop.  
  
 **Error ID:** BC30783  
  
### To correct this error  
  
1.  If the `Continue For` statement is in a `Do...Loop`, change the statement to `Continue Do`.  
  
     —or—  
  
     If the `Continue For` statement is in a `While...End While` loop, change the statement to `Continue While`.  
  
2.  Otherwise, remove the `Continue For` statement.  
  
## See Also  
 [Continue Statement](../Topic/Continue%20Statement%20\(Visual%20Basic\).md)   
 [For...Next Statement](../Topic/For...Next%20Statement%20\(Visual%20Basic\).md)