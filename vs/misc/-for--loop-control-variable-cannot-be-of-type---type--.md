---
title: "&#39;For&#39; loop control variable cannot be of type &#39;&lt;type&gt;&#39;"
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
  - "vbc30337"
  - "bc30337"
helpviewer_keywords: 
  - "BC30337"
ms.assetid: 988bba15-e9a2-4045-98a0-7f53c8b2c3e3
caps.latest.revision: 9
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
# &#39;For&#39; loop control variable cannot be of type &#39;&lt;type&gt;&#39;
You have attempted to use a loop control variable that is not a valid type. At the beginning of a `For` loop, the start point, the end point, and the step value are evaluated in textual order. All three expressions must be implicitly convertible to the type of the variable. If the `For` loop variable is of type `Object`, then at least one of the expressions at run time must be of a numeric type, and all three expressions must be coercible to the widest numeric type among them.  
  
 **Error ID:** BC30337  
  
### To correct this error  
  
-   Check the type of the loop control variable and change it to a valid one.  
  
## See Also  
 [For (Visual Basic)](http://msdn.microsoft.com/en-us/c470a263-9b49-4308-8fd6-8592b84a7980)   
 [Do...Loop Statement](../Topic/Do...Loop%20Statement%20\(Visual%20Basic\).md)   
 [For...Next Statement](../Topic/For...Next%20Statement%20\(Visual%20Basic\).md)