---
title: "Arrays cannot be declared with &#39;New&#39;"
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
  - "vbc30053"
  - "bc30053"
helpviewer_keywords: 
  - "BC30053"
ms.assetid: aa55f3b7-2045-497b-9543-5ec6e2b74fe2
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
# Arrays cannot be declared with &#39;New&#39;
The `New` keyword can appear only in the initialization part of an array declaration. This means `New` must be on the right side of the equal sign (`=`) so it can create a new array type to be assigned to the array variable.  
  
 The shortcut for class initialization is not available for arrays. The following two code lines are both valid and are equivalent because they initialize an object from a class.  
  
```  
Dim formA as Form = New Form  
Dim formA as New Form  
```  
  
 However, array initialization cannot use the same shortcut as class initialization.  
  
 Note that the `New` clause for an array must contain both parentheses, `()`, and braces, `{}`. The parentheses specify that the new type is an array, and the braces supply the initialization values. The compiler requires the braces even if they are empty, that is, even if you are not initializing any of the array values.  
  
 **Error ID:** BC30053  
  
### To correct this error  
  
-   Replace a statement such as `Dim myDates() As New Date` with a statement such as `Dim myDates() As Date = New Date() {}`.  
  
## See Also  
 [Arrays](../Topic/Arrays%20in%20Visual%20Basic.md)   
 [How to: Initialize an Array Variable in Visual Basic](../Topic/How%20to:%20Initialize%20an%20Array%20Variable%20in%20Visual%20Basic.md)