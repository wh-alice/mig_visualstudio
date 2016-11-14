---
title: "&#39;End Class&#39; must be preceded by a matching &#39;Class&#39; | Microsoft Docs"
ms.custom: ""
ms.date: "2015-07-20"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc30460"
  - "bc30460"
helpviewer_keywords: 
  - "BC30460"
ms.assetid: 0e6989da-f281-4ac4-8579-b6d627be8de8
caps.latest.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
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
 [End \<keyword> Statement](http://msdn.microsoft.com/en-us/Library/42d6e088-ab0f-4cda-88e8-fdce3e5fcf4f)