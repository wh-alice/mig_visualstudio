---
title: "No accessible non-generic &#39;&lt;procedurename&gt;&#39; found | Microsoft Docs"
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
  - "vbc32117"
  - "bc32117"
helpviewer_keywords: 
  - "BC32117"
ms.assetid: a7bf8b67-8a0a-499e-9992-dc00e09b7ff4
caps.latest.revision: 4
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
# No accessible non-generic &#39;&lt;procedurename&gt;&#39; found
A statement calls a procedure that has more than one overloaded version, but all the overloaded versions are generic and the call does not supply type arguments.  
  
 If there is only one generic version and you call it without type arguments, the compiler can attempt *type inference*. For more information, see "Type Inference" in [Generic Procedures in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-procedures). However, if there is more than one generic version, the compiler is not able to choose among them unless you supply type arguments. If you supply one type argument, you must supply a type argument for every type parameter that one of the overloaded versions defines.  
  
 **Error ID:** BC32117  
  
### To correct this error  
  
-   Call the procedure with a type argument list.  
  
## See Also  
 [Overloads](/dotnet/visual-basic/language-reference/modifiers/overloads)   
 [Procedure Overloading](/dotnet/visual-basic/language-reference/procedures/procedure-overloading)   
 [Generic Types in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-types)   
 [Generic Procedures in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-procedures)