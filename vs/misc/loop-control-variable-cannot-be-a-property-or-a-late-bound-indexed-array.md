---
title: "Loop control variable cannot be a property or a late-bound indexed array"
ms.custom: na
ms.date: "10/13/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "bc30039"
  - "vbc30039"
helpviewer_keywords: 
  - "BC30039"
ms.assetid: 63846449-b1df-4626-bf99-36fa9b187799
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
# Loop control variable cannot be a property or a late-bound indexed array
The variable used to iterate through a `For` loop must be of a numeric data type.  
  
 **Error ID:** BC30039  
  
### To correct this error  
  
-   Change the declaration of the loop control variable to specify `Integer`, `Short`, `Long`, `Byte`, `Single`, `Double`, or `Decimal`.  
  
## See Also  
 [For...Next Statement](../Topic/For...Next%20Statement%20\(Visual%20Basic\).md)