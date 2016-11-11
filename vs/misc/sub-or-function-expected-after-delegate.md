---
title: "&#39;Sub&#39; or &#39;Function&#39; expected after &#39;Delegate&#39; | Microsoft Docs"
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
  - "vbc30278"
  - "bc30278"
helpviewer_keywords: 
  - "BC30278"
ms.assetid: fee206b9-8dc0-436f-9909-abd8c17957f8
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
# &#39;Sub&#39; or &#39;Function&#39; expected after &#39;Delegate&#39;
A `Delegate` statement does not specify a `Sub` or `Function` procedure. The `Sub` or `Function` keyword must immediately follow the `Delegate` keyword.  
  
 **Error ID:** BC30278  
  
### To correct this error  
  
1.  Add the `Sub` or `Function` keyword immediately after `Delegate`.  
  
2.  Specify a procedure name, argument list, and return type as appropriate.  
  
## See Also  
 [Delegate Statement](/dotnet/visual-basic/language-reference/statements/delegate-statement)   
 [Procedures](/dotnet/visual-basic/language-reference/procedures/index)