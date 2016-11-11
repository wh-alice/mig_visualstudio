---
title: "&#39;In&#39; expected | Microsoft Docs"
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
  - "bc36607"
  - "vbc36607"
helpviewer_keywords: 
  - "BC36607"
ms.assetid: f390bca5-12fe-4fe1-bd86-7f8ab66dfbd8
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
# &#39;In&#39; expected
A `From` or `Aggregate` clause has been specified without an `In` operator. You use the `In` operator to identify the collection to query.  
  
 **Error ID:** BC36607  
  
### To correct this error  
  
1.  Add the `In` operator and key fields to the `From` or `Aggregate` clause. The following is an example:  
  
    ```vb#  
    Dim names = From pers In people   
                Select pers.FirstName, pers.LastName  
    ```  
  
## See Also  
 [From Clause](/dotnet/visual-basic/language-reference/queries/from-clause)   
 [Aggregate Clause](/dotnet/visual-basic/language-reference/queries/aggregate-clause)   
 [Introduction to LINQ in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/linq/introduction-to-linq)   
 [LINQ](/dotnet/visual-basic/programming-guide/language-features/linq/index)