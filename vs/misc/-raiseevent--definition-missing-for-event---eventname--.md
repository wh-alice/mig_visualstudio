---
title: "&#39;RaiseEvent&#39; definition missing for event &#39;&lt;eventname&gt;&#39;"
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
  - "vbc31132"
  - "bc31132"
helpviewer_keywords: 
  - "BC31132"
ms.assetid: 8f3442fd-2ed1-4dbc-83a8-f0860ec022ac
caps.latest.revision: 7
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
# &#39;RaiseEvent&#39; definition missing for event &#39;&lt;eventname&gt;&#39;
If an event is declared as `Custom`, it must supply a procedure for raising the event.  
  
 **Error ID:** BC31132  
  
### To correct this error  
  
1.  Include a `RaiseEvent` declaration between the `Custom Event` statement and the `End Event` statement.  
  
2.  Verify that other procedures within the event declaration are correctly terminated.  
  
## See Also  
 [RaiseEvent Statement](../Topic/RaiseEvent%20Statement.md)   
 [Event Statement](../Topic/Event%20Statement.md)