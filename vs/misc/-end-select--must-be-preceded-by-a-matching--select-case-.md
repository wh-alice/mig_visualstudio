---
title: "&#39;End Select&#39; must be preceded by a matching &#39;Select Case&#39;"
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
  - "bc30088"
  - "vbc30088"
helpviewer_keywords: 
  - "BC30088"
ms.assetid: 9de8c0d4-4ce9-45cf-98d6-8f68bba507a5
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
# &#39;End Select&#39; must be preceded by a matching &#39;Select Case&#39;
An `End Select` statement occurs without a corresponding `Select` or `Select Case` statement. `End Select` must be preceded by a `Select` or `Select Case` statement.  
  
 **Error ID:** BC30088  
  
### To correct this error  
  
1.  If this `Select` block is part of a set of nested `Select` blocks, make sure each block is properly terminated.  
  
2.  Verify that other control structures within the `Select` block are correctly terminated.  
  
3.  Check that this `Select` block is correctly formatted.  
  
## See Also  
 [Select...Case Statement](../Topic/Select...Case%20Statement%20\(Visual%20Basic\).md)