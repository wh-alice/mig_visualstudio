---
title: "&#39;AddHandler&#39; and &#39;RemoveHandler&#39; methods must have exactly one parameter"
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
  - "vbc31133"
  - "bc31133"
helpviewer_keywords: 
  - "BC31133"
ms.assetid: f6295626-dd63-408c-ab5f-76367f94d6ca
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
# &#39;AddHandler&#39; and &#39;RemoveHandler&#39; methods must have exactly one parameter
A custom event declaration must have `AddHandler` or `RemoveHandler` declarations, each of which takes a single parameter of the delegate type specified by the custom event's `As` clause.  
  
 **Error ID:** BC31133  
  
### To correct this error  
  
-   Remove the extra parameters from the parameter list, and change the parameter type to be the same as the delegate type specified by the custom event's `As` clause.  
  
## Example  
 This example shows a custom event with the correct parameter types for the `AddHandler` and `RemoveHandler` declarations.  
  
 [!code[VbVbalrEventError#1](../misc/codesnippet/VisualBasic/-addhandler--and--removehandler--methods-must-have-exactly-one-parameter_1.vb)]  
  
## See Also  
 [Event Statement](../Topic/Event%20Statement.md)   
 [AddHandler - delete](http://msdn.microsoft.com/en-us/fc464cf8-582c-48a6-a9c2-185c4c3d5ff8)   
 [RemoveHandler - delete](http://msdn.microsoft.com/en-us/35c17f61-6e22-4b87-b6e1-3ed0c27a88a0)   
 [Events](../Topic/Events%20\(Visual%20Basic\).md)