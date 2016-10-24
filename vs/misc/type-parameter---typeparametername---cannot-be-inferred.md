---
title: "Type parameter &#39;&lt;typeparametername&gt;&#39; cannot be inferred | testtitle"
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
  - "bc36572"
  - "vbc36572"
helpviewer_keywords: 
  - "BC36572"
ms.assetid: 02264070-b055-4ab0-8d2a-eac4d90d9fdf
caps.latest.revision: 4
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
# Type parameter &#39;&lt;typeparametername&gt;&#39; cannot be inferred
A generic procedure is called without supplying a type argument list, and type inference fails for one of the type arguments.  
  
 When you call a generic procedure, you normally supply a type argument for each type parameter defined by the procedure. However, you have the alternative of omitting the type argument list entirely. When you do this, the compiler attempts to infer the type of each type argument from the context of your call. For more information, see "Type Inference" in [Generic Procedures in Visual Basic](../Topic/Generic%20Procedures%20in%20Visual%20Basic.md).  
  
 **Error ID:** BC36572  
  
### To correct this error  
  
-   Make sure the types of the normal arguments are such that type inference is consistent with the type parameters declared for the generic procedure.  
  
     -or-  
  
-   Call the generic procedure with a complete type argument list, so that type inference is not necessary.  
  
## See Also  
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Type List](../Topic/Type%20List%20\(Visual%20Basic\).md)   
 [Generic Procedures in Visual Basic](../Topic/Generic%20Procedures%20in%20Visual%20Basic.md)