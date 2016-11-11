---
title: "&#39;&lt;attributename&gt;&#39; cannot be applied more than once to an assembly | Microsoft Docs"
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
  - "bc31521"
  - "vbc31521"
helpviewer_keywords: 
  - "BC31521"
ms.assetid: 7312570f-8afb-4afe-992f-b6f7796f5f26
caps.latest.revision: 8
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
# &#39;&lt;attributename&gt;&#39; cannot be applied more than once to an assembly
The specified attribute can only be applied once to an attribute.  
  
 **Error ID:** BC31521  
  
### To correct this error  
  
1.  Remove redundant applications of this attribute.  
  
2.  If you are using a custom attribute you developed, modify `AttributeUsageAttribute` and set the `AllowMultiple` property to `True`.  
  
## See Also  
 <xref:System.AttributeUsageAttribute>   
 <xref:System.AttributeUsageAttribute.AllowMultiple%2A?displayProperty=fullName>