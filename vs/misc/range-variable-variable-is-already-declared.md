---
title: "Range variable &lt;variable&gt; is already declared | Microsoft Docs"
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
  - "vbc36600"
  - "bc36600"
helpviewer_keywords: 
  - "BC36600"
ms.assetid: d53da04d-cd36-44ec-8b23-48cd81231191
caps.latest.revision: 4
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
# Range variable &lt;variable&gt; is already declared
A range variable name specified in a `Select` clause, or the `Into` part of an `Aggregate`, `Group By`, or `Group Join` clause, duplicates the name of a range variable already specified in the query clause.  
  
 **Error ID:** BC36600  
  
### To correct this error  
  
1.  Ensure that all range variables in a query clause have unique names.  
  
## See Also  
 [Introduction to LINQ in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/linq/introduction-to-linq)   
 [Aggregate Clause](/dotnet/visual-basic/language-reference/queries/aggregate-clause)   
 [Select Clause](/dotnet/visual-basic/language-reference/queries/select-clause)   
 [Group By Clause](/dotnet/visual-basic/language-reference/queries/group-by-clause)   
 [Group Join Clause](/dotnet/visual-basic/language-reference/queries/group-join-clause)