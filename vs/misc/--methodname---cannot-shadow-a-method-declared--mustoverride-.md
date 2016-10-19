---
title: "&#39;&lt;methodname&gt;&#39; cannot shadow a method declared &#39;MustOverride&#39;"
ms.custom: ""
ms.date: "10/13/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc31404"
  - "bc31404"
helpviewer_keywords: 
  - "BC31404"
ms.assetid: 3e7bb4a0-14af-46ba-bc62-2234c16f1827
caps.latest.revision: 8
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
# &#39;&lt;methodname&gt;&#39; cannot shadow a method declared &#39;MustOverride&#39;
A property or method with the `MustOverride` modifier and the same name is declared in a deriving class.  
  
 **Error ID:** BC31404  
  
### To correct this error  
  
1.  Add the `Overrides` modifier to the overriding property or method in the derived class.  
  
2.  Remove the `MustOverride` modifier from the property or method in the base class.  
  
## See Also  
 [MustOverride](../Topic/MustOverride%20\(Visual%20Basic\).md)