---
title: "&#39;Group&#39; or an identifier expected | Microsoft Docs"
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
  - "vbc36707"
  - "bc36707"
helpviewer_keywords: 
  - "BC36707"
ms.assetid: 214e4aa3-d20f-41b3-902c-f1076d31b832
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
# &#39;Group&#39; or an identifier expected
The `Into` portion of a `Group By` or `Group Join` clause does not include the `Group` keyword. You must include the `Group` keyword in the `Into` clause of a `Group By` or `Group Join` clause to identify the variable name to use for the grouped results. This can be either a name you specify or the keyword `Group`.  
  
 **Error ID:** BC36707  
  
### To correct this error  
  
1.  Ensure that the `Into` portion of the `Group By` or `Group Join` clause includes the `Group` keyword, as shown in the following example.  
  
    ```vb#  
    Dim orders = From order In orderList _  
                 Order By order.OrderDate _  
                 Group By OrderDate = order.OrderDate _  
                 Into OrdersByDate = Group  
    ```  
  
## See Also  
 [Introduction to LINQ in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/linq/introduction-to-linq)   
 [Group By Clause](/dotnet/visual-basic/language-reference/queries/group-by-clause)   
 [Group Join Clause](/dotnet/visual-basic/language-reference/queries/group-join-clause)