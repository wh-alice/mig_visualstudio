---
title: "&#39;Return&#39; statement in a Function, Get, or Operator must return a value"
ms.custom: ""
ms.date: "10/13/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bc30654"
  - "vbc30654"
helpviewer_keywords: 
  - "BC30654"
ms.assetid: af0fb1fc-1b2e-4cae-9768-10965cda5506
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
# &#39;Return&#39; statement in a Function, Get, or Operator must return a value
`Return` statements must be used to return a value to a calling procedure. You cannot use `Return` statements by themselves to control program flow.  
  
 **Error ID:** BC30654  
  
### To correct this error  
  
1.  Specify a value that the function or procedure can return.  
  
2.  Use the `End` statement to cause the program to exit the current procedure.  
  
## See Also  
 [Return Statement](../Topic/Return%20Statement%20\(Visual%20Basic\).md)   
 [End \<keyword> Statement](../Topic/End%20%3Ckeyword%3E%20Statement%20\(Visual%20Basic\).md)