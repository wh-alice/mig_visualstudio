---
title: "&#39;Exit AddHandler&#39;, &#39;Exit RemoveHandler&#39; and &#39;Exit RaiseEvent&#39; are not valid | testtitle"
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
  - "vbc31111"
  - "bc31111"
helpviewer_keywords: 
  - "BC31111"
ms.assetid: e02264f3-0645-4de5-b622-8a2a74496b64
caps.latest.revision: 9
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
# &#39;Exit AddHandler&#39;, &#39;Exit RemoveHandler&#39; and &#39;Exit RaiseEvent&#39; are not valid
'Exit AddHandler', 'Exit RemoveHandler' and 'Exit RaiseEvent' are not valid. Use 'Return' to exit from event members.  
  
 The `Exit` statement cannot be used to exit `AddHandler`, `RemoveHandler`, or `RaiseEvent` methods in a `Custom Event` declaration. Instead, use the `Return` statement, without specifying a return expression, to exit the method.  
  
 **Error ID:** BC31111  
  
### To correct this error  
  
-   Replace the `Exit` statement with a `Return` statement.  
  
     Make sure the `Return` statement does not specify a return expression.  
  
## See Also  
 [Event Statement](../Topic/Event%20Statement.md)   
 [AddHandler - delete](http://msdn.microsoft.com/en-us/fc464cf8-582c-48a6-a9c2-185c4c3d5ff8)   
 [RemoveHandler - delete](http://msdn.microsoft.com/en-us/35c17f61-6e22-4b87-b6e1-3ed0c27a88a0)   
 [RaiseEvent - delete](http://msdn.microsoft.com/en-us/7f765da0-5491-40b6-9ed5-24c98f9daad9)   
 [Return Statement](../Topic/Return%20Statement%20\(Visual%20Basic\).md)   
 [Events](../Topic/Events%20\(Visual%20Basic\).md)