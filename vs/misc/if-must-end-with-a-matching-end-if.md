---
title: "&#39;If&#39; must end with a matching &#39;End If&#39; | Microsoft Docs"
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
  - "bc30081"
  - "vbc30081"
helpviewer_keywords: 
  - "BC30081"
ms.assetid: e5905d59-56bb-4daf-aca5-5ff847fc62f6
caps.latest.revision: 9
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
# &#39;If&#39; must end with a matching &#39;End If&#39;
An `If` statement occurs without a corresponding `End If` statement. An `End If` statement must be used to end the `If` block.  
  
 **Error ID:** BC30081  
  
### To correct this error  
  
1.  If this `If` block is part of a set of nested `If` blocks, make sure each block is properly terminated.  
  
2.  Add an `End If` statement to the end of the `If` block.  
  
## See Also  
 [If...Then...Else Statement](/dotnet/visual-basic/language-reference/statements/if-then-else-statement)