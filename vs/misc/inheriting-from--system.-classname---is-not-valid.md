---
title: "Inheriting from &#39;System.&lt;classname&gt;&#39; is not valid"
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
  - "vbc30015"
  - "bc30015"
helpviewer_keywords: 
  - "BC30015"
ms.assetid: b4c005df-a510-47c7-b5cc-27f4514d32b6
caps.latest.revision: 9
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
# Inheriting from &#39;System.&lt;classname&gt;&#39; is not valid
A class cannot inherit from `System.Array`, `System.Delegate`, `System.Enum`, or `System.ValueType`.  
  
 **Error ID:** BC30015  
  
### To correct this error  
  
-   Remove the `Inherits` statement or change it to inherit from a valid base class.  
  
## See Also  
 [Inheritance Basics](../Topic/Inheritance%20Basics%20\(Visual%20Basic\).md)   
 [Object Variable Declaration](../Topic/Object%20Variable%20Declaration%20\(Visual%20Basic\).md)