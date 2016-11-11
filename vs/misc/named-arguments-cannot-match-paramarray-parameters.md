---
title: "Named arguments cannot match ParamArray parameters | Microsoft Docs"
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
  - "vbrNamedArgumentOnParamArray"
ms.assetid: ba35fb86-329a-4ceb-864b-045c07661482
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
# Named arguments cannot match ParamArray parameters
Parameter arrays must be passed by value.  
  
### To correct this error  
  
1.  Pass the arguments `ByVal`, rather than by naming them.  
  
## See Also  
 [Parameter Arrays](/dotnet/visual-basic/language-reference/procedures/parameter-arrays)   
 [Passing Arguments by Value and by Reference](/dotnet/visual-basic/language-reference/procedures/passing-arguments-by-value-and-by-reference)   
 [Passing Arguments by Position and by Name](/dotnet/visual-basic/language-reference/procedures/passing-arguments-by-position-and-by-name)