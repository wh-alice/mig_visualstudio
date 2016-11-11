---
title: "Arguments cannot be passed to a &#39;New&#39; used on a type parameter | Microsoft Docs"
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
  - "BC32085"
  - "vbc32085"
helpviewer_keywords: 
  - "BC32085"
ms.assetid: a60bf62d-2b2e-4621-b8db-e67720b918fb
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
# Arguments cannot be passed to a &#39;New&#39; used on a type parameter
A declaration or assignment statement invokes a generic type and supplies constructor arguments to a type parameter that has the [New Operator](/dotnet/visual-basic/language-reference/operators/new-operator) constraint.  
  
 A constraint list on a type parameter can specify that the type argument passed to that type parameter must expose a parameterless constructor that the creating code can access. A type parameter cannot require a constructor that takes parameters, and a type parameter with the `New` constraint cannot accept such a constructor.  
  
 **Error ID:** BC32085  
  
### To correct this error  
  
-   Remove the argument list following the type argument in the statement invoking the generic type. You cannot pass constructor arguments to the corresponding type parameter.  
  
## See Also  
 [Generic Types in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-types)   
 [Value Types and Reference Types](/dotnet/visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types)