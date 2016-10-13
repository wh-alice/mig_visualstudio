---
title: "&#39;Next&#39; statement names more variables than there are matching &#39;For&#39; statements"
ms.custom: na
ms.date: "10/01/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "bc32037"
  - "vbc32037"
helpviewer_keywords: 
  - "BC32037"
ms.assetid: 7c97d835-1043-40ec-a645-63a053f5f916
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
# &#39;Next&#39; statement names more variables than there are matching &#39;For&#39; statements
Nested loops are terminated with a single `Next` statement that specifies more loop variables than there are loops in the nest, as in the following example:  
  
```  
For I = 1 To 10  
   For J = 1 To 5  
      ' ...  
Next J, I, K   ' Next J, I is valid, but there is no loop on K.  
```  
  
 **Error ID:** BC32037  
  
### To correct this error  
  
1.  Ensure that the `Next` statement specifies all the nested loop variables in the reverse order of loop initiation.  
  
2.  Remove any extraneous variables from the `Next` statement.  
  
## See Also  
 [For...Next Statement](../Topic/For...Next%20Statement%20\(Visual%20Basic\).md)