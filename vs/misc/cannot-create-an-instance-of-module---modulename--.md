---
title: "Cannot create an instance of Module &#39;&lt;modulename&gt;&#39;"
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
  - "bc30166"
  - "vbc30166"
helpviewer_keywords: 
  - "BC30166"
ms.assetid: 40b9dbd3-9b57-450f-a631-b0ab06ca19c4
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
# Cannot create an instance of Module &#39;&lt;modulename&gt;&#39;
A module exists only as a single shared instance, and additional instances cannot be created.  
  
 **Error ID:** BC30166  
  
### To correct this error  
  
-   Change the module to a class, or replace it in the `New` clause with a class name.  
  
## See Also  
 [Module Statement](../Topic/Module%20Statement.md)   
 [NOT IN BUILD: Implements Keyword and Implements Statement](http://msdn.microsoft.com/en-us/b96560f7-6413-480f-a1e2-f80253bab5be)