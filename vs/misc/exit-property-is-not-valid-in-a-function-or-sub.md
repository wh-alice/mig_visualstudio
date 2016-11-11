---
title: "&#39;Exit Property&#39; is not valid in a Function or Sub | Microsoft Docs"
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
  - "vbc30066"
  - "bc30066"
helpviewer_keywords: 
  - "BC30066"
ms.assetid: 09e7e766-e35d-4282-b949-d227f733f950
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
# &#39;Exit Property&#39; is not valid in a Function or Sub
`Exit Property` appears in a `Function` procedure or a `Sub` procedure. An `Exit` statement must match the block in which it occurs.  
  
 **Error ID:** BC30066  
  
### To correct this error  
  
-   Replace the `Exit Property` with the `Exit Function` or `Exit Sub` statement as appropriate.  
  
## See Also  
 [Sub Procedures](/dotnet/visual-basic/language-reference/procedures/sub-procedures)   
 [Function Procedures](/dotnet/visual-basic/language-reference/procedures/function-procedures)   
 [Property Procedures](/dotnet/visual-basic/language-reference/procedures/property-procedures)