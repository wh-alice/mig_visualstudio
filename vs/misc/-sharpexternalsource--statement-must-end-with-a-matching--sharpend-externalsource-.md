---
title: "&#39;#ExternalSource&#39; statement must end with a matching &#39;#End ExternalSource&#39; | Microsoft Docs"
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
  - "vbc30579"
  - "bc30579"
helpviewer_keywords: 
  - "BC30579"
ms.assetid: 8d658008-eddc-4b7d-a8d4-036da42957bf
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
# &#39;#ExternalSource&#39; statement must end with a matching &#39;#End ExternalSource&#39;
The `#ExternalSource` directive references outside code, enabling the compiler to accurately report when exceptions occur within that code. An `#ExternalSource` block must begin with `#ExternalSource` and end with `#End ExternalSource`.  
  
 **Error ID:** BC30579  
  
### To correct this error  
  
1.  Add `#End ExternalSource` to the appropriate location in your code.  
  
2.  Remove the initial `#ExternalSource` if it is unnecessary.  
  
## See Also  
 [#ExternalSource Directive](../Topic/%23ExternalSource%20Directive.md)   
 [NOTINBUILD Conditional Compilation (Visual Basic)](http://msdn.microsoft.com/en-us/ad1e35e0-935e-4a35-a2ae-738bcf2a9240)