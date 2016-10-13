---
title: "&#39;Case Else&#39; can only appear inside a &#39;Select Case&#39; statement"
ms.custom: na
ms.date: "10/01/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "bc30071"
  - "vbc30071"
helpviewer_keywords: 
  - "BC30071"
ms.assetid: 9a4f8ccb-717a-4d18-91b4-4a373202c38a
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
# &#39;Case Else&#39; can only appear inside a &#39;Select Case&#39; statement
A `Case Else` statement occurs outside a `Select` block. A `Case Else` statement can be used only between a `Select` or `Select Case` statement and its corresponding `End Select` statement.  
  
 **Error ID:** BC30071  
  
### To correct this error  
  
-   Remove the `Case Else` statement or move it to within a `Select` block.  
  
## See Also  
 [Select...Case Statement](../Topic/Select...Case%20Statement%20\(Visual%20Basic\).md)