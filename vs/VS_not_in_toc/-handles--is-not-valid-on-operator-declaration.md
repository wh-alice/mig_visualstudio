---
title: "&#39;Handles&#39; is not valid on operator declaration"
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
  - "bc33003"
  - "vbc33003"
helpviewer_keywords: 
  - "BC33003"
ms.assetid: 8336402c-9393-4e8e-834d-55c2268f24f6
caps.latest.revision: 11
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
# &#39;Handles&#39; is not valid on operator declaration
An [Operator Statement](../Topic/Operator%20Statement.md) specifies the [Handles](../Topic/Handles%20Clause%20\(Visual%20Basic\).md) keyword.  
  
 Only a `Sub` procedure can handle events. An `Operator` procedure cannot. For more information on event handlers, see [How to: Call an Event Handler in Visual Basic](../Topic/How%20to:%20Call%20an%20Event%20Handler%20in%20Visual%20Basic.md).  
  
 An `Operator` procedure requires both the `Public` and `Shared` keywords, and a conversion operator requires either the `Widening` or the `Narrowing` keyword. For more information, see [Operator Procedures](../Topic/Operator%20Procedures%20\(Visual%20Basic\).md).  
  
 **Error ID:** BC33003  
  
### To correct this error  
  
-   If you intend this procedure to handle events, rewrite it as a `Sub` procedure.  
  
-   If you intend this procedure to define an operator, remove the `Handles` keyword from its declaration.  
  
## See Also  
 [Operator Statement](../Topic/Operator%20Statement.md)   
 [How to: Define an Operator](../Topic/How%20to:%20Define%20an%20Operator%20\(Visual%20Basic\).md)   
 [How to: Define a Conversion Operator](../Topic/How%20to:%20Define%20a%20Conversion%20Operator%20\(Visual%20Basic\).md)