---
title: "&#39;End Class&#39; must be preceded by a matching &#39;Class&#39;"
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
  - "vbc30460"
  - "bc30460"
helpviewer_keywords: 
  - "BC30460"
ms.assetid: 0e6989da-f281-4ac4-8579-b6d627be8de8
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
# &#39;End Class&#39; must be preceded by a matching &#39;Class&#39;
`End Class` is used to complete a `Class` block; hence it can only appear at the end of the block. Either you have a redundant `End Class`, or your `End Class` statement appears outside the bounds of its corresponding `Class` block.  
  
 **Error ID:** BC30460  
  
### To correct this error  
  
-   Locate and remove any redundant `End Class` statements.  
  
-   Move the `End Class` statement to the appropriate location in your code.  
  
## See Also  
 [End \<keyword> Statement](../Topic/End%20%3Ckeyword%3E%20Statement%20\(Visual%20Basic\).md)