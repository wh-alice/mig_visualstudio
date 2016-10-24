---
title: "Methods or events that implement interface members cannot be declared &#39;Shared&#39;"
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
  - "bc30505"
  - "vbc30505"
helpviewer_keywords: 
  - "BC30505"
ms.assetid: a24937c5-aeac-47de-a08b-d8696dd8221a
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
# Methods or events that implement interface members cannot be declared &#39;Shared&#39;
You have attempted to declare as `Shared` a method or event that implements an interface member. Methods and events being implemented in a class cannot be designated `Shared` or `Private`, except in a non-inheritable class.  
  
 **Error ID:** BC30505  
  
### To correct this error  
  
-   Remove the `Shared` keyword.  
  
## See Also  
 [Shared](../Topic/Shared%20\(Visual%20Basic\).md)