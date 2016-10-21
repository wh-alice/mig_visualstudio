---
title: "Methods declared in structures cannot have &#39;Handles&#39; clauses"
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
  - "vbc30728"
  - "bc30728"
helpviewer_keywords: 
  - "BC30728"
ms.assetid: 64c70bb5-3696-4865-8194-328394c2b4b1
caps.latest.revision: 10
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
# Methods declared in structures cannot have &#39;Handles&#39; clauses
Structure methods cannot use the `Handles` keyword to handle events.  
  
 **Error ID:** BC30728  
  
### To correct this error  
  
-   Consider redesigning your structure as a class.  
  
     You can use `AddHandler` to associate an event with an event handler in a structure, provided that the structure implements an event handler defined in an interface.  
  
## See Also  
 [Structures and Classes](../Topic/Structures%20and%20Classes%20\(Visual%20Basic\).md)   
 [NOT IN BUILD: Classes: Blueprints for Objects](http://msdn.microsoft.com/en-us/2c86373d-0333-4616-a7d8-4790c4e89f7b)   
 [Events](../Topic/Events%20\(Visual%20Basic\).md)   
 [NOT IN BUILD:AddHandler and RemoveHandler](http://msdn.microsoft.com/en-us/a7a24bd2-519a-46fe-8a2c-2b9df2ca28ef)