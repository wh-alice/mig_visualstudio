---
title: "Properties declared &#39;WriteOnly&#39; cannot have a &#39;Get&#39; | testtitle"
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
  - "bc30023"
  - "vbc30023"
helpviewer_keywords: 
  - "BC30023"
ms.assetid: ac290f7d-cbc3-4979-a5d9-1ae1bb26e79d
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
# Properties declared &#39;WriteOnly&#39; cannot have a &#39;Get&#39;
The `Get` procedure reads the value of a property. `WriteOnly` properties cannot be read.  
  
 **Error ID:** BC30023  
  
### To correct this error  
  
-   Remove the `WriteOnly` keyword from the `Property` statement, or remove the `Get` procedure from the property body.  
  
## See Also  
 [Property Statement](../Topic/Property%20Statement.md)   
 [Get Statement](../Topic/Get%20Statement.md)   
 [WriteOnly](../Topic/WriteOnly%20\(Visual%20Basic\).md)