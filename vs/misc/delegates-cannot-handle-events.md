---
title: "Delegates cannot handle events | Microsoft Docs"
ms.custom: ""
ms.date: "10/20/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bc30019"
  - "vbc30019"
helpviewer_keywords: 
  - "BC30019"
ms.assetid: 7f0c7bb9-8e81-44bf-acc5-80d9785708aa
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
# Delegates cannot handle events
A delegate is a reference type that points to a shared procedure or to an instance procedure on an object. Because the procedure it points to can be changed by assignment, the `Delegate` statement cannot support the `Handles` or `Implements` clauses.  
  
 **Error ID:** BC30019  
  
### To correct this error  
  
-   Remove the `Handles` clause from the `Delegate` statement.  
  
## See Also  
 [NOT IN BUILD: Delegates and the AddressOf Operator](http://msdn.microsoft.com/en-us/7b2ed932-8598-4355-b2f7-5cedb23ee86f)   
 [Delegate Statement](../Topic/Delegate%20Statement.md)   
 [Handles](../Topic/Handles%20Clause%20\(Visual%20Basic\).md)   
 [Implements Statement](../Topic/Implements%20Statement.md)