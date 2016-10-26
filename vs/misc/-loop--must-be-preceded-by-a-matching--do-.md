---
title: "&#39;Loop&#39; must be preceded by a matching &#39;Do&#39;"
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
  - "vbc30091"
  - "bc30091"
helpviewer_keywords: 
  - "BC30091"
ms.assetid: 05f47b2f-4eaa-4911-981e-3fce737d249f
caps.latest.revision: 9
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
# &#39;Loop&#39; must be preceded by a matching &#39;Do&#39;
A `Loop` statement occurs without a corresponding `Do` statement. `Loop` must be preceded by a corresponding `Do` statement.  
  
 **Error ID:** BC30091  
  
### To correct this error  
  
1.  If this `Do` loop is part of a set of nested `Do` loops, make sure each loop is properly terminated.  
  
2.  Verify that other control structures within the `Do` loop are correctly terminated.  
  
3.  Ensure that this `Do` loop is correctly formatted.  
  
## See Also  
 [Do...Loop Statement](../Topic/Do...Loop%20Statement%20\(Visual%20Basic\).md)