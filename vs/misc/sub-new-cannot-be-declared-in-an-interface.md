---
title: "&#39;Sub New&#39; cannot be declared in an interface | Microsoft Docs"
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
  - "bc30363"
  - "vbc30363"
helpviewer_keywords: 
  - "BC30363"
ms.assetid: 371d9aa8-a935-48ce-ada2-0a69ba20e070
caps.latest.revision: 10
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
# &#39;Sub New&#39; cannot be declared in an interface
You have attempted to declare `Sub New` within an interface. Because it is a constructor, `Sub New` can run only once when a class is created. It cannot be called explicitly from anywhere other than the first line of code in another constructor in either the same class or a derived class.  
  
 **Error ID:** BC30363  
  
### To correct this error  
  
-   Remove the `Sub New` or move it to a more appropriate place in your code.  
  
## See Also  
 [NOT IN BUILD: Using Constructors and Destructors](http://msdn.microsoft.com/en-us/548eebe1-86c4-4377-b2f5-447cb8be3d90)