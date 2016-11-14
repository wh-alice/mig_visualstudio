---
title: "Only conversion operators can be declared &#39;&lt;keyword&gt;&#39; | Microsoft Docs"
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
  - "bc33019"
  - "vbc33019"
helpviewer_keywords: 
  - "BC33019"
ms.assetid: 946266fe-a909-41b1-aad4-f85dc8050b88
caps.latest.revision: 9
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
# Only conversion operators can be declared &#39;&lt;keyword&gt;&#39;
An [Operator Statement](/dotnet/visual-basic/language-reference/statements/operator-statement) specifies [Widening](/dotnet/visual-basic/language-reference/modifiers/widening) or [Narrowing](/dotnet/visual-basic/language-reference/modifiers/narrowing) when the operator is not a conversion operator.  
  
 Every operator must be declared as both [Public](/dotnet/visual-basic/language-reference/modifiers/public) and [Shared](/dotnet/visual-basic/language-reference/modifiers/shared). However, only a conversion operator can be declared with [Widening](/dotnet/visual-basic/language-reference/modifiers/widening) or [Narrowing](/dotnet/visual-basic/language-reference/modifiers/narrowing), but not both.  
  
 An operator definition can optionally include the [Overloads](/dotnet/visual-basic/language-reference/modifiers/overloads) and [Shadows](/dotnet/visual-basic/language-reference/modifiers/shadows) keywords. No other keywords are permitted in an [Operator Statement](/dotnet/visual-basic/language-reference/statements/operator-statement).  
  
 **Error ID:** BC33019  
  
### To correct this error  
  
1.  Remove the `Widening` or `Narrowing` keyword from the operator definition. These do not apply, because no type conversion is taking place.  
  
## See Also  
 [Operator Procedures](/dotnet/visual-basic/language-reference/procedures/operator-procedures)   
 [Operator Statement](/dotnet/visual-basic/language-reference/statements/operator-statement)   
 [How to: Define an Operator](http://msdn.microsoft.com/en-us/Library/d4b0e253-092a-4e6e-9fe2-01f562140a29)   
 [How to: Define a Conversion Operator](http://msdn.microsoft.com/en-us/Library/54203dfa-c24b-463f-9942-d5153e89e762)   
 [Type Conversions in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/data-types/type-conversions)