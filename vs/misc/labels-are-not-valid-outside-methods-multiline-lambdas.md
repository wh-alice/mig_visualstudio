---
title: "Labels are not valid outside methods-multiline lambdas | Microsoft Docs"
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
  - "vbc30016"
  - "bc30016"
helpviewer_keywords: 
  - "BC30016"
ms.assetid: 17d12a96-d759-4df9-882c-5e45c1d814a5
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
# Labels are not valid outside methods/multiline lambdas
You can add a label to a statement only within a `Sub`, `Function`, property `Get`, or property `Set` procedure. Only an executable statement can have a label, and all executable statements must be inside procedures.  
  
 **Error ID:** BC30016  
  
### To correct this error  
  
1.  Remove the label from the statement, or move the statement inside a procedure.  
  
## See Also  
 [How to: Label Statements](http://msdn.microsoft.com/en-us/Library/38f1ff43-2054-42cb-963b-1998e60c6ed4)   
 [Sub Statement](/dotnet/visual-basic/language-reference/statements/sub-statement)   
 [Function Statement](/dotnet/visual-basic/language-reference/statements/function-statement)   
 [Get Statement](/dotnet/visual-basic/language-reference/statements/get-statement)   
 [Set Statement](/dotnet/visual-basic/language-reference/statements/set-statement)