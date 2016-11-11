---
title: "No accessible &#39;&lt;genericprocedurename&gt;&#39; accepts this number of type arguments | Microsoft Docs"
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
  - "bc32118"
  - "vbc32118"
helpviewer_keywords: 
  - "BC32118"
ms.assetid: 4ee942ba-0fa1-4ec1-9c2c-a0c0dc3f1b17
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
# No accessible &#39;&lt;genericprocedurename&gt;&#39; accepts this number of type arguments
A statement calls a generic procedure that has more than one overloaded version, but none of the overloaded versions defines the same number of type parameters as the number of type arguments supplied in the call.  
  
 If there is only one generic version, you call it without type arguments, and the compiler can attempt *type inference*. For more information, see "Type Inference" in [Generic Procedures in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-procedures). However, if there is more than one generic version, the compiler is not able to choose among them unless you supply type arguments. If you supply one type argument, you must supply a type argument for every type parameter that one of the overloaded versions defines.  
  
 **Error ID:** BC32118  
  
### To correct this error  
  
-   Decide which overloaded version you want to call, and then supply the appropriate number of type arguments.  
  
## See Also  
 [Overloads](/dotnet/visual-basic/language-reference/modifiers/overloads)   
 [Procedure Overloading](/dotnet/visual-basic/language-reference/procedures/procedure-overloading)   
 [Generic Types in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-types)   
 [Generic Procedures in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-procedures)