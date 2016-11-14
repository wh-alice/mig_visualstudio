---
title: "&#39;Join&#39; expected | Microsoft Docs"
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
  - "vbc36631"
  - "bc36631"
helpviewer_keywords: 
  - "BC36631"
ms.assetid: bb2b03b6-6784-423a-b91a-cb7066c1d093
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
# &#39;Join&#39; expected
A `Group Join` clause has been specified without a `Join` keyword.  
  
 **Error ID:** BC36631  
  
### To correct this error  
  
1.  Add the `Join` keyword to the `Group Join` clause, as shown in the following example:  
  
    ```vb#  
    Dim query = From var1 In collection1 _  
                Join var2 In collection2 _  
                Group Join var3 In collection3 _  
                On var2.ID Equals var3 Into Matches = Group _  
                On var1 Equals var2.ID _  
                Select JoinID = var1, var2.Name, Matches  
    ```  
  
## See Also  
 [How to: Combine Data with Joins](http://msdn.microsoft.com/en-us/Library/5b00a478-035b-41c6-8918-be1a97728396)   
 [Group Join Clause](/dotnet/visual-basic/language-reference/queries/group-join-clause)   
 [Introduction to LINQ in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/linq/introduction-to-linq)   
 [LINQ](/dotnet/visual-basic/programming-guide/language-features/linq/index)