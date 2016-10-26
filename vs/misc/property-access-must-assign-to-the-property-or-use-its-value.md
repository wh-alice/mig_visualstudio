---
title: "Property access must assign to the property or use its value"
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
  - "bc30545"
  - "vbc30545"
helpviewer_keywords: 
  - "BC30545"
ms.assetid: df271c05-1e7a-44e8-bf53-79f06ef916ab
caps.latest.revision: 10
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
# Property access must assign to the property or use its value
You have tried to access a property without assigning to it or using its value. The following code provides an example:  
  
 [!CODE [VbVbalrErrorSamples#1](VbVbalrErrorSamples#1)]  
  
 **Error ID:** BC30545  
  
### To correct this error  
  
-   Assign a value to the property, as shown in the following example:  
  
     [!CODE [VbVbalrErrorSamples#3](VbVbalrErrorSamples#3)]  
  
     \- or -  
  
-   Use the value of the property, as shown in the following example:  
  
     [!CODE [VbVbalrErrorSamples#2](VbVbalrErrorSamples#2)]  
  
## See Also  
 [Property Procedures](../Topic/Property%20Procedures%20\(Visual%20Basic\).md)   
 [Assignment Operators](../Topic/Assignment%20Operators%20\(Visual%20Basic\).md)