---
title: "Overload resolution failed because no accessible &#39;&lt;genericprocedurename&gt;&#39; accepts this number of type arguments | Microsoft Docs"
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
  - "bc32087"
  - "vbc32087"
helpviewer_keywords: 
  - "BC32087"
ms.assetid: a3eaafd3-80f6-4b7d-9b75-47b043fe17b5
caps.latest.revision: 11
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
# Overload resolution failed because no accessible &#39;&lt;genericprocedurename&gt;&#39; accepts this number of type arguments
A call to an overloaded generic procedure cannot be resolved because the compiler cannot access any overloaded version with the appropriate number of type parameters.  
  
 When you call a generic procedure, you must supply one type argument for each type parameter. Alternatively, you can supply no type arguments at all and let the compiler attempt to do *type inference*. For more information, see "Type Inference" in [Generic Procedures in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-procedures).  
  
 **Error ID:** BC32087  
  
### To correct this error  
  
1.  Ensure that the version you intend to call is accessible by the calling code. See [Access Levels in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/declared-elements/access-levels).  
  
2.  Add or remove type arguments from your calling code so that the type argument list matches the type parameter list of the version you intend to call.  
  
     -or-  
  
     Remove all type arguments from your calling code and let the compiler attempt to do type inference. Be aware that type inference can fail if there are conflicts or ambiguities.  
  
## See Also  
 [Overloaded Properties and Methods](/dotnet/visual-basic/programming-guide/language-features/objects-and-classes/overloaded-properties-and-methods)   
 [Overload Resolution](/dotnet/visual-basic/language-reference/procedures/overload-resolution)   
 [Generic Types in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-types)   
 [Type List](/dotnet/visual-basic/language-reference/statements/type-list)