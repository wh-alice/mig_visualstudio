---
title: "&#39;ReadOnly&#39; property &#39;&lt;propertyname&gt;&#39; cannot be the target of an assignment"
ms.custom: na
ms.date: "10/01/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "bc30098"
  - "vbc30098"
helpviewer_keywords: 
  - "BC30098"
ms.assetid: d0c6cdac-a49d-49d2-ba92-ddf01eed0620
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
# &#39;ReadOnly&#39; property &#39;&lt;propertyname&gt;&#39; cannot be the target of an assignment
A `ReadOnly` property occurs in a context that assigns a value to it. Only writable variables, properties, and array elements can have values assigned to them during execution.  
  
 **Error ID:** BC30098  
  
### To correct this error  
  
-   Remove the `ReadOnly` keyword from the `Property` statement declaring the variable, or remove the statement that assigns a value to it.  
  
## See Also  
 [ReadOnly](../Topic/ReadOnly%20\(Visual%20Basic\).md)   
 [Property Statement](../Topic/Property%20Statement.md)