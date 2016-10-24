---
title: "&#39;#End Region&#39; must be preceded by a matching &#39;#Region&#39;"
ms.custom: ""
ms.date: "10/20/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc30680"
  - "bc30680"
helpviewer_keywords: 
  - "BC30680"
ms.assetid: 1ea60620-c8dc-4957-8cf4-07b25d20da3b
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
# &#39;#End Region&#39; must be preceded by a matching &#39;#Region&#39;
With `#Region` you can specify a block of code to expand or collapse when using the outlining feature of the [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] Code Editor. The start and end of `#Region` statements must be in the same code block.  
  
 **Error ID:** BC30680  
  
### To correct this error  
  
-   Insert `#Region` at the appropriate place before the corresponding `#End``Region` statement.  
  
## See Also  
 [#Region Directive](../Topic/%23Region%20Directive.md)