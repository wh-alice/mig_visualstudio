---
title: "&#39;#ElseIf&#39; cannot follow &#39;#Else&#39; as part of an &#39;#If&#39; block | hehe"
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
  - "bc32030"
  - "vbc32030"
helpviewer_keywords: 
  - "BC32030"
ms.assetid: 248d6464-3019-4753-8a33-7070bbe5d2a6
caps.latest.revision: 14
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
# &#39;#ElseIf&#39; cannot follow &#39;#Else&#39; as part of an &#39;#If&#39; block
An `#ElseIf` conditional compilation directive follows an `#Else` directive. `#Else` must be the last directive in the conditional block before the `#End If` directive.  
  
 **Error ID:** BC32030  
  
### To correct this error  
  
1.  Check if the preceding `#Else` should be an `#ElseIf`.  
  
2.  Check that a preceding `#If` block is properly terminated and that a new `#If` block is initiated.  
  
3.  If everything else is correct, move this `#ElseIf` directive and its corresponding statement block to precede the `#Else` block.  
  
## See Also  
 [#If...Then...#Else Directives](../Topic/%23If...Then...%23Else%20Directives.md)