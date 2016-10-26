---
title: "&#39;AddHandler&#39; and &#39;RemoveHandler&#39; method parameters cannot be declared &#39;ByRef&#39;"
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
  - "vbc31134"
  - "bc31134"
helpviewer_keywords: 
  - "BC31134"
ms.assetid: 942f0b91-e71a-499a-ad10-a5dfcb4e72b1
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
# &#39;AddHandler&#39; and &#39;RemoveHandler&#39; method parameters cannot be declared &#39;ByRef&#39;
The parameters of the `AddHandler` and `RemoveHandler` methods cannot be declared with the `ByRef` modifier.  
  
 **Error ID:** BC31134  
  
### To correct this error  
  
-   Remove the `ByRef` keyword from the parameter.  
  
## See Also  
 [Event Statement](../Topic/Event%20Statement.md)   
 [AddHandler - delete](http://msdn.microsoft.com/en-us/fc464cf8-582c-48a6-a9c2-185c4c3d5ff8)   
 [RemoveHandler - delete](http://msdn.microsoft.com/en-us/35c17f61-6e22-4b87-b6e1-3ed0c27a88a0)   
 [ByRef](../Topic/ByRef%20\(Visual%20Basic\).md)   
 [Events](../Topic/Events%20\(Visual%20Basic\).md)