---
title: "&#39;!&#39; requires its left operand to have a type parameter, class or interface type, but this operand has the type &#39;&lt;type&gt;&#39; | Microsoft Docs"
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
  - "vbc30103"
  - "bc30103"
helpviewer_keywords: 
  - "BC30103"
ms.assetid: 95982e5e-c3e5-402e-ad7b-4c5076a13869
caps.latest.revision: 10
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
# &#39;!&#39; requires its left operand to have a type parameter, class or interface type, but this operand has the type &#39;&lt;type&gt;&#39;
Dictionary member access, which uses an exclamation point (`!`) instead of a period (`.`), is valid only on a class or an interface.  
  
 **Error ID:** BC30103  
  
### To correct this error  
  
-   Replace the expression on the left of the exclamation point with one that evaluates to a defined class or interface type.  
  
## See Also  
 [Special Characters in Code](/dotnet/visual-basic/programming-guide/program-structure/special-characters-in-code)