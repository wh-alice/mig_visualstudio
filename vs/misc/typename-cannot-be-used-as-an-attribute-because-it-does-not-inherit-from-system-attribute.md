---
title: "&#39;&lt;typename&gt;&#39; cannot be used as an attribute because it does not inherit from &#39;System.Attribute&#39; | Microsoft Docs"
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
  - "vbc31504"
  - "bc31504"
helpviewer_keywords: 
  - "BC31504"
ms.assetid: 37517623-5099-4db9-a461-f2f5daa4957b
caps.latest.revision: 10
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
# &#39;&lt;typename&gt;&#39; cannot be used as an attribute because it does not inherit from &#39;System.Attribute&#39;
An attempt was made to use a class that is not derived from `System.Attribute`.  
  
 **Error ID:** BC31504  
  
### To correct this error  
  
1.  Define custom attributes as classes that derive from `System.Attribute` by adding an `Imports` statement to the first line of code in the class.  
  
## See Also  
 <xref:System.AttributeUsageAttribute>   
 [NOT IN BUILD: Custom Attributes in Visual Basic](http://msdn.microsoft.com/en-us/d72d8a5c-8f64-4614-b15b-cad66845d047)