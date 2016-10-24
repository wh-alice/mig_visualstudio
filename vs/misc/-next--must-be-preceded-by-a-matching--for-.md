---
title: "&#39;Next&#39; must be preceded by a matching &#39;For&#39; | Microsoft Docs"
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
  - "vbc30092"
  - "bc30092"
helpviewer_keywords: 
  - "BC30092"
ms.assetid: 4bf49bb2-c69b-443d-aa58-cb40fcfb1370
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
# &#39;Next&#39; must be preceded by a matching &#39;For&#39;
A `Next` statement occurs without a corresponding `For` or `For Each` statement. `Next` must be preceded by a corresponding `For` or `For Each` statement.  
  
 **Error ID:** BC30092  
  
### To correct this error  
  
1.  If this `For` loop is part of a set of nested `For` loops, make sure each loop is properly terminated.  
  
2.  Verify that other control structures within the `For` loop are correctly terminated.  
  
3.  Ensure that this `For` loop is correctly formatted.  
  
## See Also  
 [For...Next Statement](../Topic/For...Next%20Statement%20\(Visual%20Basic\).md)   
 [For Each...Next Statement](../Topic/For%20Each...Next%20Statement%20\(Visual%20Basic\).md)