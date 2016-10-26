---
title: "&#39;&lt;specifier&gt;&#39; is not valid on an interface method declaration"
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
  - "bc30270"
  - "vbc30270"
helpviewer_keywords: 
  - "BC30270"
ms.assetid: 598f2944-3e5d-4686-b6f7-2b4bcaf5c211
caps.latest.revision: 8
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
# &#39;&lt;specifier&gt;&#39; is not valid on an interface method declaration
A `Function` or `Sub` statement inside an interface contains an invalid keyword, such as `Implements`. An interface can only define members, not implement them.  
  
 **Error ID:** BC30270  
  
### To correct this error  
  
1.  Remove the invalid keyword from the declaration statement.  
  
2.  Move the implementation of interface members to a class that implements the interface.  
  
## See Also  
 [Interface Statement](../Topic/Interface%20Statement%20\(Visual%20Basic\).md)   
 [Implements Statement](../Topic/Implements%20Statement.md)