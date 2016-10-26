---
title: "&#39;#ExternalSource&#39; directives cannot be nested"
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
  - "bc30580"
  - "vbc30580"
helpviewer_keywords: 
  - "BC30580"
ms.assetid: 56c6ef4b-28b1-4a62-8afa-d83a7742b507
caps.latest.revision: 13
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
# &#39;#ExternalSource&#39; directives cannot be nested
You attempted to place an `#ExternalSource` directive within another `#ExternalSource` block. The `#ExternalSource` directive references outside code, enabling the compiler to accurately report when exceptions occur within that code.  
  
 `#ExternalSource` blocks cannot be nested within other `#ExternalSource` blocks.  
  
 **Error ID:** BC30580  
  
### To correct this error  
  
-   Move the inner `#ExternalSource` directive outside the enclosing `#ExternalSource` block.  
  
## See Also  
 [#ExternalSource Directive](../Topic/%23ExternalSource%20Directive.md)   
 [NOTINBUILD Conditional Compilation (Visual Basic)](http://msdn.microsoft.com/en-us/ad1e35e0-935e-4a35-a2ae-738bcf2a9240)