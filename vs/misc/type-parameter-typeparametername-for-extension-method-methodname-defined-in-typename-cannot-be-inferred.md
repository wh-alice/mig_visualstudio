---
title: "Type parameter &#39;&lt;typeparametername&gt;&#39; for extension method &#39;&lt;methodname&gt;&#39; defined in &#39;&lt;typename&gt;&#39; cannot be inferred | Microsoft Docs"
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
  - "vbc36589"
  - "bc36589"
helpviewer_keywords: 
  - "BC36589"
ms.assetid: 4676a7a5-934b-4b74-b640-48065fc07e94
caps.latest.revision: 5
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
# Type parameter &#39;&lt;typeparametername&gt;&#39; for extension method &#39;&lt;methodname&gt;&#39; defined in &#39;&lt;typename&gt;&#39; cannot be inferred
A generic extension method is called without supplying a type argument list, and type inference fails for one of the type arguments.  
  
 When you call a generic procedure, you normally supply a type argument for each type parameter defined by the procedure. However, you have the alternative of omitting the type argument list entirely. When you do this, the compiler attempts to infer the type of each type argument from the context of your call. For more information, see "Type Inference" in [Generic Procedures in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-procedures).  
  
 **Error ID:** BC36589  
  
### To correct this error  
  
-   Make sure the types of the normal arguments are such that type inference is consistent with the type parameters declared for the generic procedure.  
  
     -or-  
  
-   Call the generic procedure with a complete type argument list, so that type inference is not necessary.  
  
## See Also  
 [Extension Methods](/dotnet/visual-basic/language-reference/procedures/extension-methods)   
 [Generic Types in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-types)   
 [Type List](/dotnet/visual-basic/language-reference/statements/type-list)   
 [Generic Procedures in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-procedures)