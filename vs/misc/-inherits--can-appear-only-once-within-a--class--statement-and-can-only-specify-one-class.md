---
title: "&#39;Inherits&#39; can appear only once within a &#39;Class&#39; statement and can only specify one class | Microsoft Docs"
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
  - "vbc30121"
  - "bc30121"
helpviewer_keywords: 
  - "BC30121"
ms.assetid: 4ac5b018-5632-4661-8ac6-dbda2f8c4dfe
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
# &#39;Inherits&#39; can appear only once within a &#39;Class&#39; statement and can only specify one class
More than one `Inherits` statement appears in the same class, or an `Inherits` statement specifies more than one class. A class can inherit from only one base class.  
  
 **Error ID:** BC30121  
  
### To correct this error  
  
-   Remove any extra `Inherits` statements and make sure the remaining `Inherits` statement specifies only one base class.  
  
## See Also  
 [Inherits Statement](../Topic/Inherits%20Statement.md)   
 [Inheritance Basics](../Topic/Inheritance%20Basics%20\(Visual%20Basic\).md)