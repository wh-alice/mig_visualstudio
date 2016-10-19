---
title: "&#39;&lt;method&gt;&#39; is not accessible in this context because it is &#39;&lt;modifier&gt;&#39;"
ms.custom: ""
ms.date: "10/13/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc30389"
  - "bc30389"
helpviewer_keywords: 
  - "BC30389"
ms.assetid: fae58a68-df91-4741-a8c9-f1bb10e166e2
caps.latest.revision: 9
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
# &#39;&lt;method&gt;&#39; is not accessible in this context because it is &#39;&lt;modifier&gt;&#39;
You have attempted to access a method that is not accessible in this context because it has been declared `Private`. A possible cause for this error is that the [!INCLUDE[vbprvb](../codequality/includes/vbprvb_md.md)] compiler imports all members of a class and is case-insensitive, so names differentiated only by casing may collide.  
  
 **Error ID:** BC30389  
  
### To correct this error  
  
-   Consider declaring the method `Public`.  
  
-   If the error is caused by a name collision, differentiate the colliding names by more than case.  
  
## See Also  
 [Private](../Topic/Private%20\(Visual%20Basic\).md)