---
title: "&#39;Return&#39; statement in a Sub or a Set cannot return a value | Microsoft Docs"
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
  - "bc30647"
  - "vbc30647"
helpviewer_keywords: 
  - "BC30647"
ms.assetid: d4c05c28-d650-4f49-976e-650d84802036
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
# &#39;Return&#39; statement in a Sub or a Set cannot return a value
`Sub` procedures and property `Set` procedures cannot return values.  
  
 **Error ID:** BC30647  
  
### To correct this error  
  
-   Change the current procedure to a function, or to a `Get` property procedure if the current procedure is part of a property.  
  
-   You can effectively return values from `Sub` procedures by modifying the value of parameters passed by reference using the `ByRef` keyword.  
  
## See Also  
 [Return Statement](/dotnet/visual-basic/language-reference/statements/return-statement)   
 [Sub Procedures](/dotnet/visual-basic/language-reference/procedures/sub-procedures)   
 [Function Procedures](/dotnet/visual-basic/language-reference/procedures/function-procedures)   
 [Property Procedures](/dotnet/visual-basic/language-reference/procedures/property-procedures)