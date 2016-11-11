---
title: "Syntax error in cast operator; two arguments separated by comma are required | Microsoft Docs"
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
  - "vbc30944"
  - "bc30944"
helpviewer_keywords: 
  - "BC30944"
ms.assetid: 1f7ed4a1-6ff5-4836-8424-21618c68ff45
caps.latest.revision: 6
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
# Syntax error in cast operator; two arguments separated by comma are required
An expression uses the `CType` conversion function or the `DirectCast` or `TryCast` conversion keyword but supplies only one argument.  
  
 `CType`, `DirectCast`, and `TryCast` all require two arguments. The first is an expression to be converted and the second is the data type or class type to which to convert it.  
  
 **Error ID:** BC30944  
  
### To correct this error  
  
-   Supply both arguments as required for the conversion.  
  
-   If you intend to use one of the specific [Type Conversion Functions](/dotnet/visual-basic/language-reference/functions/type-conversion-functions) such as `CString`, you must use that function name instead of `CType`. Then only one argument is required.  
  
## See Also  
 [CType Function](/dotnet/visual-basic/language-reference/functions/ctype-function)   
 [DirectCast Operator](/dotnet/visual-basic/language-reference/operators/directcast-operator)   
 [TryCast Operator](/dotnet/visual-basic/language-reference/operators/trycast-operator)   
 [Type Conversion Functions](/dotnet/visual-basic/language-reference/functions/type-conversion-functions)