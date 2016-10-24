---
title: "Statements and labels are not valid between &#39;Select Case&#39; and first &#39;Case&#39; | testtitle"
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
  - "bc30058"
  - "vbc30058"
helpviewer_keywords: 
  - "BC30058"
ms.assetid: 399b4659-f7df-4377-80be-43019f1e6206
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
# Statements and labels are not valid between &#39;Select Case&#39; and first &#39;Case&#39;
A statement that is not a comment appears between the opening `Select` or `Select Case` statement and its first `Case` statement.  
  
 **Error ID:** BC30058  
  
### To correct this error  
  
-   If the intervening statement is a comment, precede it with a comment delimiter (`'` or `REM`). Otherwise, move or delete the statement.  
  
## See Also  
 [Select...Case Statement](../Topic/Select...Case%20Statement%20\(Visual%20Basic\).md)