---
title: "Type character cannot be used in a &#39;Sub&#39; declaration because a &#39;Sub&#39; doesn&#39;t return a value | Microsoft Docs"
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
  - "bc30303"
  - "vbc30303"
helpviewer_keywords: 
  - "BC30303"
ms.assetid: f5a744f0-d312-4fe3-90cd-3cf372a93664
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
# Type character cannot be used in a &#39;Sub&#39; declaration because a &#39;Sub&#39; doesn&#39;t return a value
A `Sub` procedure, like a `Function` procedure, is a separate procedure that can take arguments and perform a series of statements. Unlike a `Function` procedure, a `Sub` does not return a value, and therefore cannot contain a type declaration.  
  
 **Error ID:** BC30303  
  
### To correct this error  
  
-   Change the `Sub` procedure to a `Function` procedure.  
  
## See Also  
 [Sub Procedures](/dotnet/visual-basic/language-reference/procedures/sub-procedures)   
 [Function Procedures](/dotnet/visual-basic/language-reference/procedures/function-procedures)