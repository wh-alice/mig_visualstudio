---
title: "&#39;.&#39; expected | Microsoft Docs"
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
  - "bc30287"
  - "vbc30287"
helpviewer_keywords: 
  - "BC30287"
ms.assetid: 7d7b4934-b521-4ed3-b054-aeb71f8daacf
caps.latest.revision: 12
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
# &#39;.&#39; expected
The code has a `Handles` clause that contains an exclamation point (`!`).  
  
 **Error ID:** BC30287  
  
### To correct this error  
  
1.  If the `Handles` clause refers to an event within an object, use a period (`.`) to separate the object from the event.  
  
     This example handles the `Click` event from the `Button1` object.  
  
     [!code-vb[VbVbalrEventError#21](../misc/codesnippet/VisualBasic/dot-expected_1.vb)]  
  
## See Also  
 [Handles](/dotnet/visual-basic/language-reference/statements/handles-clause)