---
title: "&#39;Do&#39; must end with a matching &#39;Loop&#39;"
ms.custom: na
ms.date: "10/13/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "vbc30083"
  - "bc30083"
helpviewer_keywords: 
  - "BC30083"
ms.assetid: b157b9e3-57fa-4324-a13d-b37bcf0861e6
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
# &#39;Do&#39; must end with a matching &#39;Loop&#39;
A `Do` statement occurs without a corresponding `Loop` statement. A `Loop` statement must be used to end the `Do` loop.  
  
 **Error ID:** BC30083  
  
### To correct this error  
  
-   If this `Do` loop is part of a set of nested loops, make sure each loop is properly terminated.  
  
-   Add a `Loop` statement to the end of the `Do` loop.  
  
## See Also  
 [Do...Loop Statement](../Topic/Do...Loop%20Statement%20\(Visual%20Basic\).md)