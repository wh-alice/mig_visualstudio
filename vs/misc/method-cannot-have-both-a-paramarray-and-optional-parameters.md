---
title: "Method cannot have both a ParamArray and Optional parameters"
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
  - "vbc30046"
  - "bc30046"
helpviewer_keywords: 
  - "BC30046"
ms.assetid: 41066df8-c9ee-4f67-9f6c-4f62e3abc7be
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
# Method cannot have both a ParamArray and Optional parameters
A `ParamArray` argument is automatically optional, and it must be the only optional argument in the procedure declaration. All preceding arguments must be required.  
  
 **Error ID:** BC30046  
  
### To correct this error  
  
-   Remove the optional arguments in the declaration.  
  
## See Also  
 [Parameter Arrays](../Topic/Parameter%20Arrays%20\(Visual%20Basic\).md)   
 [ParamArray](../Topic/ParamArray%20\(Visual%20Basic\).md)