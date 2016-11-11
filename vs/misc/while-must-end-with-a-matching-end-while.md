---
title: "&#39;While&#39; must end with a matching &#39;End While&#39; | Microsoft Docs"
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
  - "bc30082"
  - "vbc30082"
helpviewer_keywords: 
  - "BC30082"
ms.assetid: 50b722b1-906f-4cb1-b5d4-fefab2ba3907
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
# &#39;While&#39; must end with a matching &#39;End While&#39;
A `While` statement occurs without a corresponding `End While` statement. An `End While` statement must be used to end the `While` block.  
  
 **Error ID:** BC30082  
  
### To correct this error  
  
1.  If this `While` block is part of a set of nested `While` blocks, make sure each block is properly terminated.  
  
2.  Add an `End While` statement to the end of the `While` block.  
  
## See Also  
 [While...End While Statement](/dotnet/visual-basic/language-reference/statements/while-end-while-statement)