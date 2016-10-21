---
title: "Arguments cannot be passed to a &#39;New&#39; used on a type parameter"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "BC32085"
  - "vbc32085"
helpviewer_keywords: 
  - "BC32085"
ms.assetid: a60bf62d-2b2e-4621-b8db-e67720b918fb
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
# Arguments cannot be passed to a &#39;New&#39; used on a type parameter
A declaration or assignment statement invokes a generic type and supplies constructor arguments to a type parameter that has the [New Operator](../Topic/New%20Operator%20\(Visual%20Basic\).md) constraint.  
  
 A constraint list on a type parameter can specify that the type argument passed to that type parameter must expose a parameterless constructor that the creating code can access. A type parameter cannot require a constructor that takes parameters, and a type parameter with the `New` constraint cannot accept such a constructor.  
  
 **Error ID:** BC32085  
  
### To correct this error  
  
-   Remove the argument list following the type argument in the statement invoking the generic type. You cannot pass constructor arguments to the corresponding type parameter.  
  
## See Also  
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Value Types and Reference Types](../Topic/Value%20Types%20and%20Reference%20Types.md)