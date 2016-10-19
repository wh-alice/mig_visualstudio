---
title: "&#39;New&#39; cannot be used on a type parameter that does not have a &#39;New&#39; constraint"
ms.custom: ""
ms.date: "10/13/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bc32046"
  - "vbc32046"
helpviewer_keywords: 
  - "BC32046"
ms.assetid: 7ec6b52d-6fd5-47a0-b4a2-163bfd3dae35
caps.latest.revision: 8
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
# &#39;New&#39; cannot be used on a type parameter that does not have a &#39;New&#39; constraint
A declaration statement uses a [New Operator](../Topic/New%20Operator%20\(Visual%20Basic\).md) clause specifying a type parameter as the type to be created, and the type parameter is declared without a `New` constraint.  
  
 A *constraint* on a type parameter imposes a requirement on any type argument passed to that type parameter when the generic type is created. The `New` constraint specifies that the type argument must expose a parameterless constructor that the creating code can access. This is what allows a `New` clause in a declaration statement to create an instance of that type.  
  
 **Error ID:** BC32046  
  
### To correct this error  
  
-   If you can require the type argument to expose an accessible parameterless constructor, add the `New` constraint to the declaration of the type parameter.  
  
-   If you cannot require the type argument to expose an accessible parameterless constructor, remove the `New` clause from the declaration statement. You cannot guarantee that any type argument passed to that type parameter permits creation of an instance.  
  
## See Also  
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Type List](../Topic/Type%20List%20\(Visual%20Basic\).md)