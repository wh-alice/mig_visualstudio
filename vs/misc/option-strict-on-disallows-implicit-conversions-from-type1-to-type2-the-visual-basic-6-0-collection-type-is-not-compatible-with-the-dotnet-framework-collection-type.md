---
title: "Option Strict On disallows implicit conversions from &#39;&lt;type1&gt;&#39; to &#39;&lt;type2&gt;&#39;; the Visual Basic 6.0 collection type is not compatible with the .NET Framework collection type | Microsoft Docs"
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
  - "vbc30753"
  - "bc30753"
helpviewer_keywords: 
  - "BC30753"
ms.assetid: 7e1bb22e-a507-483e-bfd6-f3a43e24a232
caps.latest.revision: 12
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
# Option Strict On disallows implicit conversions from &#39;&lt;type1&gt;&#39; to &#39;&lt;type2&gt;&#39;; the Visual Basic 6.0 collection type is not compatible with the .NET Framework collection type
`Option Strict On` disallows implicit conversions from '`<type1>`' to '`<type2>`'; the Visual Basic 6.0 collection type is not compatible with the [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] collection type.  
  
 The collection object that is used in Visual Basic 6.0 differs from the collection object that is used in [!INCLUDE[vs_current_long](../misc/includes/vs_current_long_md.md)].  
  
 **Error ID:** BC30753  
  
### To correct this error  
  
-   Explicitly convert collection objects by using one of the type conversion keywords. The [CType Function](/dotnet/visual-basic/language-reference/functions/ctype-function) and [DirectCast Operator](/dotnet/visual-basic/language-reference/operators/directcast-operator) keywords throw a run-time exception if the conversion fails. The [TryCast Operator](/dotnet/visual-basic/language-reference/operators/trycast-operator) keyword returns [Nothing](/dotnet/visual-basic/language-reference/nothing) if the conversion fails.  
  
## See Also  
 [CType Function](/dotnet/visual-basic/language-reference/functions/ctype-function)   
 [DirectCast Operator](/dotnet/visual-basic/language-reference/operators/directcast-operator)   
 [TryCast Operator](/dotnet/visual-basic/language-reference/operators/trycast-operator)   
 [Nothing](/dotnet/visual-basic/language-reference/nothing)   
 [NIB Collections in Visual Basic](http://msdn.microsoft.com/en-us/8b2b7845-2251-4573-8dd3-c9f9c0a66a21)