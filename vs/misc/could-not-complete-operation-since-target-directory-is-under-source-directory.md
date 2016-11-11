---
title: "Could not complete operation since target directory is under source directory | Microsoft Docs"
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
  - "vbrIO_CyclicOperation"
ms.assetid: 850d3a24-5d51-4ac8-a912-630efcd75278
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
# Could not complete operation since target directory is under source directory
A cyclic operation has failed. Cyclic operations cycle and therefore cannot complete. For example, Object A may attempt to inherit from Object B, which in turn inherits from Object A.  
  
### To correct this error  
  
-   When inheriting, make sure that there are no cyclic references.  
  
## See Also  
 [Error Types](/dotnet/visual-basic/programming-guide/language-features/error-types)   
 [Debugging Basics: Breakpoints](http://msdn.microsoft.com/en-us/752a02c2-0ac7-4c8b-aa1b-4b2b3b21152e)