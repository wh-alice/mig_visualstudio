---
title: "Type constraint cannot be a &#39;NotInheritable&#39; class | Microsoft Docs"
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
  - "vbc32060"
  - "bc32060"
helpviewer_keywords: 
  - "BC32060"
ms.assetid: f45cc0b6-7df1-462a-b3df-c526c143e16a
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
# Type constraint cannot be a &#39;NotInheritable&#39; class
A constraint list includes a class that is marked as [NotInheritable](/dotnet/visual-basic/language-reference/modifiers/notinheritable).  
  
 A constraint list on a type parameter can accept at most one class. A type argument supplied for that type parameter must inherit from that class. Therefore, the type parameter cannot accept a *sealed*, or `NotInheritable`, class as a constraint.  
  
 **Error ID:** BC32060  
  
### To correct this error  
  
-   If the type parameter must be able to inherit from the class, and you have control over the definition of the class, remove the `NotInheritable` declaration from the class.  
  
-   If the class must remain `NotInheritable`, you cannot use it as a constraint. Remove the class name from the constraint list.  
  
## See Also  
 [Generic Types in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-types)