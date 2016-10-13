---
title: "&#39;Exit Select&#39; can only appear inside a &#39;Select&#39; statement"
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
  - "vbc30099"
  - "bc30099"
helpviewer_keywords: 
  - "BC30099"
ms.assetid: 37c65fc8-6ad9-456a-80b8-66288c62ef24
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
# &#39;Exit Select&#39; can only appear inside a &#39;Select&#39; statement
An `Exit Select` statement occurs outside a `Select` block. `Exit Select` is valid only between a `Select` or `Select Case` statement and a corresponding `End Select` statement.  
  
 **Error ID:** BC30099  
  
### To correct this error  
  
1.  Make sure a valid `Select` or `Select Case` statement precedes the `Exit Select` and a valid `End Select` statement appears after it.  
  
2.  Verify that other control structures within the `Select` block are correctly terminated.  
  
## See Also  
 [Select...Case Statement](../Topic/Select...Case%20Statement%20\(Visual%20Basic\).md)