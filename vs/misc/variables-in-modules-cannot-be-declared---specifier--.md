---
title: "Variables in Modules cannot be declared &#39;&lt;specifier&gt;&#39;"
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
  - "bc30593"
  - "vbc30593"
helpviewer_keywords: 
  - "BC30593"
ms.assetid: 2500b776-7fa4-4272-8cc7-204593706651
caps.latest.revision: 8
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
# Variables in Modules cannot be declared &#39;&lt;specifier&gt;&#39;
You have used a specifier, such as `MustInherit`, on a variable in a `Module` statement. Modules can never be instantiated, do not support inheritance, and cannot implement interfaces.  
  
 **Error ID:** BC30593  
  
### To correct this error  
  
-   Remove the specifier.  
  
## See Also  
 [Module Statement](../Topic/Module%20Statement.md)