---
title: "&#39;Case&#39; can only appear inside a &#39;Select Case&#39; statement | Microsoft Docs"
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
  - "vbc30072"
  - "bc30072"
helpviewer_keywords: 
  - "BC30072"
ms.assetid: da808bc3-f154-444a-b547-3cf55beff8a9
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
# &#39;Case&#39; can only appear inside a &#39;Select Case&#39; statement
A `Case` statement occurs outside a `Select` block. A `Case` statement can be used only between a `Select` or `Select Case` statement and its corresponding `End Select` statement.  
  
 **Error ID:** BC30072  
  
### To correct this error  
  
-   Remove the `Case` statement or move it to within a `Select` block.  
  
## See Also  
 [Select...Case Statement](/dotnet/visual-basic/language-reference/statements/select-case-statement)