---
title: "&#39;Group&#39; not allowed in this context; identifier expected | Microsoft Docs"
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
  - "bc36708"
  - "vbc36708"
helpviewer_keywords: 
  - "BC36708"
ms.assetid: ef6b453e-68e7-47c2-997c-9fd1ca074217
caps.latest.revision: 3
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
# &#39;Group&#39; not allowed in this context; identifier expected
The `Group` keyword is included in the `Into` section of an `Aggregate` clause. The `Group` keyword is only valid in the `Group By` or `Group Join` clauses.  
  
 **Error ID:** BC36618  
  
### To correct this error  
  
-   Remove the `Group` keyword from the `Aggregate` clause. You can add a `Group By` clause to the query to group results.  
  
## See Also  
 [Aggregate Clause](/dotnet/visual-basic/language-reference/queries/aggregate-clause)   
 [Group By Clause](/dotnet/visual-basic/language-reference/queries/group-by-clause)   
 [Group Join Clause](/dotnet/visual-basic/language-reference/queries/group-join-clause)   
 [Introduction to LINQ in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/linq/introduction-to-linq)   
 [LINQ](/dotnet/visual-basic/programming-guide/language-features/linq/index)