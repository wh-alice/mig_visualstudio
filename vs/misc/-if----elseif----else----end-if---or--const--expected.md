---
title: "&#39;If&#39;, &#39;ElseIf&#39;, &#39;Else&#39;, &#39;End If&#39;, or &#39;Const&#39; expected"
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
  - "vbc30248"
  - "bc30248"
helpviewer_keywords: 
  - "BC30248"
ms.assetid: fa3bf591-8036-459c-8c29-ed7784e444f6
caps.latest.revision: 10
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
# &#39;If&#39;, &#39;ElseIf&#39;, &#39;Else&#39;, &#39;End If&#39;, or &#39;Const&#39; expected
A source line begins with a `#` character, but a valid conditional compilation directive does not immediately follow the `#`. Valid directives include `#Const`, `#ExternalSource`, `#If`, `#Else`, `#ElseIf`, `#End If`, and `#Region`.  
  
 **Error ID:** BC30248  
  
### To correct this error  
  
1.  Make sure the conditional compilation directive is spelled correctly.  
  
2.  Make sure there is no intervening space between the `#` character and the directive.  
  
3.  Remove the `#` character or add a valid directive immediately after it.  
  
## See Also  
 [Directives](../Topic/Directives%20\(Visual%20Basic\).md)