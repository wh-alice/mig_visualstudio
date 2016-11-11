---
title: "Type arguments for extension method &#39;&lt;methodName&gt;&#39; defined in &#39;&lt;typeName&gt;&#39; could not be inferred from the delegate &#39;&lt;delagateName&gt;&#39; | Microsoft Docs"
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
  - "bc36581"
  - "vbc36581"
helpviewer_keywords: 
  - "BC36581"
ms.assetid: 2bb9ca8d-7293-40e9-9285-e20b8254b3af
caps.latest.revision: 7
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
# Type arguments for extension method &#39;&lt;methodName&gt;&#39; defined in &#39;&lt;typeName&gt;&#39; could not be inferred from the delegate &#39;&lt;delagateName&gt;&#39;
An assignment statement uses `AddressOf` to assign the address of a generic extension method to a delegate, but it does not supply any type arguments to the extension method.  
  
 Normally, when you invoke a generic method, you supply a type argument for each type parameter that the generic method defines. If you do not supply any type arguments, the compiler attempts to infer the types to be passed to the type parameters. If the context does not provide enough information for the compiler to infer the types, an error is generated.  
  
 **Error ID:** BC36581  
  
### To correct this error  
  
-   In the `AddressOf` expression, specify the type arguments for the extension method.  
  
## See Also  
 [Generic Types in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-types)   
 [AddressOf Operator](/dotnet/visual-basic/language-reference/operators/addressof-operator)   
 [Generic Procedures in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-procedures)   
 [Type List](/dotnet/visual-basic/language-reference/statements/type-list)   
 [Extension Methods](/dotnet/visual-basic/language-reference/procedures/extension-methods)