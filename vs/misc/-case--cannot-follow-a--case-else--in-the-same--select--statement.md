---
title: "&#39;Case&#39; cannot follow a &#39;Case Else&#39; in the same &#39;Select&#39; statement"
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
  - "bc30321"
  - "vbc30321"
helpviewer_keywords: 
  - "BC30321"
ms.assetid: eeedbceb-2c8d-4acb-b84c-8b42c058f083
caps.latest.revision: 8
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
# &#39;Case&#39; cannot follow a &#39;Case Else&#39; in the same &#39;Select&#39; statement
A `Case Else` statement introduces statements to be executed if no match is found for the initial `Case`. A `Case` statement has been found after a `Case Else` in the same `Select` block.  
  
 **Error ID:** BC30321  
  
### To correct this error  
  
-   Move the `Case Else` to the appropriate location after the `Case` statement.  
  
## See Also  
 [Select...Case Statement](../Topic/Select...Case%20Statement%20\(Visual%20Basic\).md)