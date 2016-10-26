---
title: "&#39;#Else&#39; must be preceded by a matching &#39;#If&#39; or &#39;#ElseIf&#39;"
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
  - "vbc30028"
  - "bc30028"
helpviewer_keywords: 
  - "BC30028"
ms.assetid: c6ed34de-d6ed-4227-9880-538055aff20a
caps.latest.revision: 12
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
# &#39;#Else&#39; must be preceded by a matching &#39;#If&#39; or &#39;#ElseIf&#39;
`#Else` is a conditional compilation directive. An `#Else` directive is not preceded by a corresponding `#If` or `#ElseIf` directive.  
  
 **Error ID:** BC30028  
  
### To correct this error  
  
1.  Check that a preceding `#If` or `#ElseIf` is not separated from this `#Else` by an intervening conditional compilation block or an incorrectly placed `#End If`.  
  
2.  Check that `#Else` is preceded by another `#Else` directive. If it is, either remove `#Else` or change it to an `#ElseIf`.  
  
3.  If everything else is in order, add an `#If` directive to the beginning of the conditional compilation block.  
  
## See Also  
 [#If...Then...#Else Directives](../Topic/%23If...Then...%23Else%20Directives.md)