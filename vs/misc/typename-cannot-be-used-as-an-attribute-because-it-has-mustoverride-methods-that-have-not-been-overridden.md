---
title: "&#39;&lt;typename&gt;&#39; cannot be used as an attribute because it has &#39;MustOverride&#39; methods that have not been overridden | Microsoft Docs"
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
  - "bc31507"
  - "vbc31507"
helpviewer_keywords: 
  - "BC31507"
ms.assetid: 843643d3-3e81-4ce3-b4df-278882f3954d
caps.latest.revision: 9
author: "stevehoag"
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
# &#39;&lt;typename&gt;&#39; cannot be used as an attribute because it has &#39;MustOverride&#39; methods that have not been overridden
Classes with `MustOverride` methods cannot be used as attributes.  
  
 `MustOverride` members of attribute classes can only be used from derived classes that override such members.  
  
 **Error ID:** BC31507  
  
### To correct this error  
  
1.  Remove the `MustOverride` modifier from attribute class members.  
  
2.  Implement `MustOverride` members in a derived class, and use that class as an attribute.  
  
## See Also  
 <xref:System.AttributeUsageAttribute>   
 [NOT IN BUILD: Custom Attributes in Visual Basic](http://msdn.microsoft.com/en-us/d72d8a5c-8f64-4614-b15b-cad66845d047)