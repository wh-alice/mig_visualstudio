---
title: "Structure &#39;&lt;structurename&gt;&#39; must contain at least one instance member variable or Event declaration | Microsoft Docs"
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
  - "bc30281"
  - "vbc30281"
helpviewer_keywords: 
  - "BC30281"
ms.assetid: a03ee4e2-5fea-4933-898f-7f125b25824e
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
# Structure &#39;&lt;structurename&gt;&#39; must contain at least one instance member variable or Event declaration
A functionally empty structure occurs. At least one variable member must be declared between the `Structure` statement and the `End Structure` statement.  
  
 **Error ID:** BC30281  
  
### To correct this error  
  
-   Add a `Dim` statement or an `Event` statement to the structure.  
  
## See Also  
 [Structure Statement](../Topic/Structure%20Statement.md)   
 [Dim Statement](../Topic/Dim%20Statement%20\(Visual%20Basic\).md)   
 [Event Statement](../Topic/Event%20Statement.md)