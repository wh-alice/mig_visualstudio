---
title: "Division by zero (Visual Basic Run-Time Error) | Microsoft Docs"
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
  - "vbrID11"
ms.assetid: 5b9bc5d6-792e-48bc-a974-012e07ad95f3
caps.latest.revision: 10
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
# Division by zero (Visual Basic Run-Time Error)
An expression being used as a divisor has a value of zero.  
  
### To correct this error  
  
1.  Check the spelling of variables in the expression. A misspelled variable name can implicitly create a numeric variable that is initialized to zero.  
  
2.  Check previous operations on variables in the expression, especially those passed into the procedure as arguments from other procedures.  
  
## See Also  
 [Passing Arguments by Value and by Reference](/dotnet/visual-basic/language-reference/procedures/passing-arguments-by-value-and-by-reference)   
 [Parameter Passing Mechanism Changes in Visual Basic](http://msdn.microsoft.com/en-us/0fa2b0dc-aa1c-4797-bbd6-aa13c611cab2)