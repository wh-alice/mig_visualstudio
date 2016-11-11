---
title: "Array dimensions cannot have a negative size | Microsoft Docs"
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
  - "bc30611"
  - "vbc30611"
helpviewer_keywords: 
  - "BC30611"
ms.assetid: e310bd0d-f221-4b02-87f3-02124f4de87c
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
# Array dimensions cannot have a negative size
One or more of the array bounds specified is a negative number. You can specify a negative subscript only when you use an upper bound of -1 to declare an empty array. Such an array has zero elements, but it is not `Nothing`.  
  
 **Error ID:** BC30611  
  
### To correct this error  
  
-   Replace the negative array bound with a positive number.  
  
## See Also  
 [Arrays](/dotnet/visual-basic/programming-guide/language-features/arrays/index)