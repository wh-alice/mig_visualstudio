---
title: "&#39;WithEvents&#39; variables cannot be typed as arrays | Microsoft Docs"
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
  - "bc30476"
  - "vbc30476"
helpviewer_keywords: 
  - "BC30476"
ms.assetid: 29bed445-a247-4c88-a1eb-115535900377
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
# &#39;WithEvents&#39; variables cannot be typed as arrays
You have attempted to declare an array using `WithEvents`. You can declare as many individual variables as you like using `WithEvents`, but you cannot declare arrays that way.  
  
 **Error ID:** BC30476  
  
### To correct this error  
  
1.  Declare the variables individually.  
  
## See Also  
 [Dim Statement](/dotnet/visual-basic/language-reference/statements/dim-statement)   
 [NOT IN BUILD:WithEvents and the Handles Clause](http://msdn.microsoft.com/en-us/072b9cf6-6298-46f1-849e-4edc1631564c)