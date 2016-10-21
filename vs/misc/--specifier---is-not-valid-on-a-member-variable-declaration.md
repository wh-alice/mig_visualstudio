---
title: "&#39;&lt;specifier&gt;&#39; is not valid on a member variable declaration | hehe"
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
  - "vbc30235"
  - "bc30235"
helpviewer_keywords: 
  - "BC30235"
ms.assetid: 8c5764e4-0096-4ca0-8656-05341a39833a
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
# &#39;&lt;specifier&gt;&#39; is not valid on a member variable declaration
A `Dim` statement contains an invalid keyword. A `Dim` statement can include only the `Friend`, `Private`, `Protected`, `Public`, `ReadOnly`, `Shadows`, `Shared`, or `Static` keywords.  
  
 This message can also appear if you declare a `Static` variable outside of a procedure. You can use `Static` only at procedure level.  
  
 Note that if you include a valid keyword in a `Dim` statement, you can optionally omit the `Dim` keyword.  
  
 **Error ID:** BC30235  
  
### To correct this error  
  
1.  Remove the invalid keyword from the `Dim` statement.  
  
2.  If you have declared a `Static` variable outside of a procedure, either move the declaration inside a procedure or remove the `Static` keyword.  
  
## See Also  
 [Dim Statement](../Topic/Dim%20Statement%20\(Visual%20Basic\).md)