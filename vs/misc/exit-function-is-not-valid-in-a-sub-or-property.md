---
title: "&#39;Exit Function&#39; is not valid in a Sub or Property | Microsoft Docs"
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
  - "vbc30067"
  - "bc30067"
helpviewer_keywords: 
  - "BC30067"
ms.assetid: 207fef65-4383-4120-9e5a-e0e14d168a72
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
# &#39;Exit Function&#39; is not valid in a Sub or Property
`Exit Function` appears in a `Sub` procedure or a `Property` procedure. An `Exit` statement must match the block in which it occurs.  
  
 **Error ID:** BC30067  
  
### To correct this error  
  
-   Replace the `Exit Function` with the `Exit Sub` or `Exit Property` statement as appropriate.  
  
## See Also  
 [Sub Procedures](/dotnet/visual-basic/language-reference/procedures/sub-procedures)   
 [Function Procedures](/dotnet/visual-basic/language-reference/procedures/function-procedures)   
 [Property Procedures](/dotnet/visual-basic/language-reference/procedures/property-procedures)