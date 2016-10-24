---
title: "&#39;New&#39; cannot be used on a class that is declared &#39;MustInherit&#39; | testtitle"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc30569"
  - "bc30569"
helpviewer_keywords: 
  - "BC30569"
ms.assetid: 94c9e6a3-6489-4d58-b7e5-7b4203677e3b
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
# &#39;New&#39; cannot be used on a class that is declared &#39;MustInherit&#39;
A `MustInherit` class cannot be instantiated directly, and therefore the `New` operator cannot be used on a `MustInherit` class. Although it's possible to have variables and values whose compile time types are `MustInherit`, such variables and values will necessarily either be a null value or contain references to instances of regular classes derived from the `MustInherit` types.  
  
 **Error ID:** BC30569  
  
### To correct this error  
  
-   Remove the `New` operator.  
  
## See Also  
 [MustInherit](../Topic/MustInherit%20\(Visual%20Basic\).md)   
 [New Operator](../Topic/New%20Operator%20\(Visual%20Basic\).md)