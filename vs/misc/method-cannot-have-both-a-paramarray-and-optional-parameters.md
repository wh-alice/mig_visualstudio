---
title: "Method cannot have both a ParamArray and Optional parameters | Microsoft Docs"
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
  - "vbc30046"
  - "bc30046"
helpviewer_keywords: 
  - "BC30046"
ms.assetid: 41066df8-c9ee-4f67-9f6c-4f62e3abc7be
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
# Method cannot have both a ParamArray and Optional parameters
A `ParamArray` argument is automatically optional, and it must be the only optional argument in the procedure declaration. All preceding arguments must be required.  
  
 **Error ID:** BC30046  
  
### To correct this error  
  
-   Remove the optional arguments in the declaration.  
  
## See Also  
 [Parameter Arrays](/dotnet/visual-basic/language-reference/procedures/parameter-arrays)   
 [ParamArray](/dotnet/visual-basic/language-reference/modifiers/paramarray)