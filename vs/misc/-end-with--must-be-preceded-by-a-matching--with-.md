---
title: "&#39;End With&#39; must be preceded by a matching &#39;With&#39;"
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
  - "bc30093"
  - "vbc30093"
helpviewer_keywords: 
  - "BC30093"
ms.assetid: b0f1f7d5-0c33-4b97-8043-f0f5b40ca5d7
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
# &#39;End With&#39; must be preceded by a matching &#39;With&#39;
An `End With` statement occurs without a corresponding `With` statement. `End With` must be preceded by a corresponding `With` statement.  
  
 **Error ID:** BC30093  
  
### To correct this error  
  
1.  If this `With` block is part of a set of nested `With` blocks, make sure each block is properly terminated.  
  
2.  Verify that other control structures within the `With` block are correctly terminated.  
  
3.  Ensure that this `With` block is correctly formatted.  
  
## See Also  
 [With...End With Statement](../Topic/With...End%20With%20Statement%20\(Visual%20Basic\).md)