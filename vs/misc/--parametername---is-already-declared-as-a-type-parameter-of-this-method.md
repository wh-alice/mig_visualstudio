---
title: "&#39;&lt;parametername&gt;&#39; is already declared as a type parameter of this method | testtitle"
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
  - "bc32089"
  - "vbc32089"
helpviewer_keywords: 
  - "BC32089"
ms.assetid: 5e440b4b-f62b-4ff5-9148-2372d4752bf6
caps.latest.revision: 8
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
# &#39;&lt;parametername&gt;&#39; is already declared as a type parameter of this method
A generic procedure defines a normal parameter or a local variable with the same name as a type parameter.  
  
 Every parameter of a procedure, including every type parameter of a generic procedure, must have a name distinct from all other parameters. Because procedure parameters are used as local variables, any local variable declared within the procedure must also have a name distinct from all parameters and type parameters.  
  
 **Error ID:** BC32089  
  
### To correct this error  
  
-   Change the name of the normal parameter or local variable.  
  
## See Also  
 [Generic Procedures in Visual Basic](../Topic/Generic%20Procedures%20in%20Visual%20Basic.md)   
 [Parameter List](../Topic/Parameter%20List%20\(Visual%20Basic\).md)