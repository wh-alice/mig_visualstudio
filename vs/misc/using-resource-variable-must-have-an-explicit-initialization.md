---
title: "&#39;Using&#39; resource variable must have an explicit initialization | Microsoft Docs"
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
  - "vbc36011"
  - "bc36011"
helpviewer_keywords: 
  - "BC36011"
ms.assetid: 5db996a6-0802-4b67-91f1-4aa9c3dd6b09
caps.latest.revision: 9
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
# &#39;Using&#39; resource variable must have an explicit initialization
A `Using` statement specifies at least one resource that it does not initialize with a `New` clause.  
  
 If you have not already acquired the resource before passing control to the `Using` block, the `Using` statement must acquire the resource. To do this, it must create an object from the specified class, which requires a `New` clause.  
  
 **Error ID:** BC36011  
  
### To correct this error  
  
-   If you have already acquired the resource, use a reference variable or expression in the `Using` statement that evaluates to the acquired resource.  
  
     `Dim newFont As New System.Drawing.Font`  
  
     `Using newFont`  
  
-   If you have not already acquired the resource, add a `New` clause to the `Using` statement.  
  
     `Using newFont as`   `New`   `System.Drawing.Font`  
  
## See Also  
 [Using Statement](/dotnet/visual-basic/language-reference/statements/using-statement)   
 [New Operator](/dotnet/visual-basic/language-reference/operators/new-operator)   
 [How to: Dispose of a System Resource](../Topic/How%20to:%20Dispose%20of%20a%20System%20Resource%20\(Visual%20Basic\).md)