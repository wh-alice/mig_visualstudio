---
title: "&#39;On GoTo&#39; and &#39;On GoSub&#39; statements are no longer supported | Microsoft Docs"
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
  - "bc30817"
  - "vbc30817"
helpviewer_keywords: 
  - "BC30817"
ms.assetid: 89087bfa-7d74-4f18-9a12-2c5852076ea0
caps.latest.revision: 8
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
# &#39;On GoTo&#39; and &#39;On GoSub&#39; statements are no longer supported
It is no longer valid to use the value of a variable or expression with the `GoTo` and `GoSub` statements to control program flow.  
  
 **Error ID:** BC30817  
  
### To correct this error  
  
-   Restructure your application to use `If...Then...Else` or `Case` statements.  
  
## See Also  
 [On Error Statement](/dotnet/visual-basic/language-reference/statements/on-error-statement)   
 [If...Then...Else Statement](/dotnet/visual-basic/language-reference/statements/if-then-else-statement)   
 [Case (Visual Basic)](http://msdn.microsoft.com/en-us/a14efce6-5057-4b7d-8afd-056dd4abdcee)