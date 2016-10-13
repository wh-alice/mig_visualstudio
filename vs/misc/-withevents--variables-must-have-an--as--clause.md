---
title: "&#39;WithEvents&#39; variables must have an &#39;As&#39; clause"
ms.custom: na
ms.date: "10/01/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "vbc30412"
  - "bc30412"
helpviewer_keywords: 
  - "BC30412"
ms.assetid: 8c941523-8e5d-4bf0-8a52-772ecd5d5592
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
# &#39;WithEvents&#39; variables must have an &#39;As&#39; clause
You did not supply an `As` clause with the keyword `WithEvents`. Declare the variable as the specific class that can raise the events.  
  
 **Error ID:** BC30412  
  
### To correct this error  
  
1.  Add the `As` clause that specifies the class that can raise the events.  
  
## See Also  
 [NOT IN BUILD:WithEvents and the Handles Clause](http://msdn.microsoft.com/072b9cf6-6298-46f1-849e-4edc1631564c)   
 [Dim Statement](../Topic/Dim%20Statement%20\(Visual%20Basic\).md)