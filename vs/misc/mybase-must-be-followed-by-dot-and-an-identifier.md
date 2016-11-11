---
title: "&#39;MyBase&#39; must be followed by &#39;.&#39; and an identifier | Microsoft Docs"
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
  - "bc32027"
  - "vbc32027"
helpviewer_keywords: 
  - "BC32027"
ms.assetid: 39e5512c-ef1e-46a3-a96c-277ea24bfee2
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
# &#39;MyBase&#39; must be followed by &#39;.&#39; and an identifier
`MyBase` is not a true object variable, and it cannot appear alone. You use it only to access a member of the base class of the current instance.  
  
 **Error ID:** BC32027  
  
### To correct this error  
  
-   If you intend member access, specify the member access operator (.) and a member of the base class after `MyBase`.  
  
-   If you do not intend member access, declare and initialize an instance of the base class, or remove the reference to `MyBase`.  
  
## See Also  
 [MyBase - delete](http://msdn.microsoft.com/en-us/52491d06-6451-4f6f-9aa6-8fab59bbc2b9)   
 [Inheritance Basics](/dotnet/visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics)