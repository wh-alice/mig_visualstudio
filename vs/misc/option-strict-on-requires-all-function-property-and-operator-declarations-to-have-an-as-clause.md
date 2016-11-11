---
title: "Option Strict On requires all Function, Property, and Operator declarations to have an &#39;As&#39; clause | Microsoft Docs"
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
  - "vbc30210"
  - "bc30210"
helpviewer_keywords: 
  - "BC30210"
ms.assetid: 4d217e56-0eac-4834-bcad-234a69809390
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
# Option Strict On requires all Function, Property, and Operator declarations to have an &#39;As&#39; clause
A declaration contains a declared property or function return without an `As` clause. When `Option Strict` is `On`, every variable, property, procedure argument, and function return must be declared with an `As` clause to specify its data type; for example, `Dim MyNum As Short`.  
  
 **Error ID:** BC30210  
  
### To correct this error  
  
1.  Check to see if the `As` keyword is misspelled.  
  
2.  Supply an `As` clause for the declared property or function return, or turn `Option Strict Off`.  
  
## See Also  
 [Option Strict Statement](/dotnet/visual-basic/language-reference/statements/option-strict-statement)   
 [Property Procedures](/dotnet/visual-basic/language-reference/procedures/property-procedures)   
 [Function Procedures](/dotnet/visual-basic/language-reference/procedures/function-procedures)