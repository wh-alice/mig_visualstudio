---
title: "Operator &#39;&lt;operator&gt;&#39; must have one parameter | Microsoft Docs"
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
  - "bc33014"
  - "vbc33014"
helpviewer_keywords: 
  - "BC33014"
ms.assetid: 512a5724-a6c5-4437-a608-7d6b10e68d49
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
# Operator &#39;&lt;operator&gt;&#39; must have one parameter
A unary operator is defined with no parameters or with more than one parameter.  
  
 A unary operator must have exactly one parameter.  
  
 **Error ID:** BC33014  
  
### To correct this error  
  
-   Adjust the definition to specify exactly one parameter.  
  
-   If you need two parameters, you must define a binary operator.  
  
-   If you need no parameters or more than two, you must use the [Function Statement](/dotnet/visual-basic/language-reference/statements/function-statement) to define a `Function` procedure instead of an operator.  
  
## See Also  
 [Operator Procedures](/dotnet/visual-basic/language-reference/procedures/operator-procedures)   
 [Operator Statement](/dotnet/visual-basic/language-reference/statements/operator-statement)   
 [How to: Define an Operator](http://msdn.microsoft.com/en-us/Library/d4b0e253-092a-4e6e-9fe2-01f562140a29)   
 [How to: Define a Conversion Operator](http://msdn.microsoft.com/en-us/Library/54203dfa-c24b-463f-9942-d5153e89e762)