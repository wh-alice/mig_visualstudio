---
title: "Event &#39;&lt;eventname&gt;&#39; cannot be handled because it is not accessible from &#39;&lt;name&gt;&#39; | Microsoft Docs"
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
  - "bc30585"
  - "vbc30585"
helpviewer_keywords: 
  - "BC30585"
ms.assetid: fe039f8f-be6f-4b52-86bd-d551c54b85cd
caps.latest.revision: 8
author: "stevehoag"
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
# Event &#39;&lt;eventname&gt;&#39; cannot be handled because it is not accessible from &#39;&lt;name&gt;&#39;
You attempted to handle an event that is not accessible. For example, if a `Handles` variable is shared, the method handling the events must also be shared.  
  
 **Error ID:** BC30585  
  
### To correct this error  
  
1.  Make sure the event is accessible.  
  
## See Also  
 [NOT IN BUILD:Events and Event Handlers](http://msdn.microsoft.com/en-us/95074a0d-1cbc-4221-a95a-964185c7f962)