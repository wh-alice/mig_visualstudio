---
title: "Argument &#39;NPer&#39; must be greater than zero"
ms.custom: ""
ms.date: "10/13/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbrRate_NPerMustBeGTZero"
ms.assetid: d49242df-dbd1-4b26-bd8c-ed56d24fdfcd
caps.latest.revision: 11
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
# Argument &#39;NPer&#39; must be greater than zero
The `NPer` function, which returns a `Double` specifying the number of periods for an annuity based on periodic fixed payments and a fixed interest rate, requires an argument greater than zero.  
  
### To correct this error  
  
-   Check the spelling of arguments in the expression. A misspelled variable name can implicitly create a numeric variable that is initialized to zero.  
  
-   Check previous operations on variables in the expression, especially those passed into the procedure as arguments from other procedures.  
  
## See Also  
 [NOT IN BUILD: NPer Function](http://msdn.microsoft.com/en-us/56567d16-29f7-4928-b05f-b4cd56d4fd42)   
 [Passing Arguments by Value and by Reference](../Topic/Passing%20Arguments%20by%20Value%20and%20by%20Reference%20\(Visual%20Basic\).md)