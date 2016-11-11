---
title: "Attribute &#39;&lt;attributename&gt;&#39; cannot be applied to a module | Microsoft Docs"
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
  - "vbc30549"
  - "bc30549"
helpviewer_keywords: 
  - "BC30549"
ms.assetid: b38fea31-6b0b-4c54-9518-b59226505802
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
# Attribute &#39;&lt;attributename&gt;&#39; cannot be applied to a module
You attempted to apply an attribute to a module whose `AttributeUsageAttribute` does not specify `AttributeTargets.Module`. When the attribute was declared, it was not defined to be applied to a module.  
  
 **Error ID:** BC30549  
  
### To correct this error  
  
1.  Check the attribute declaration and specify `AttributeTargets.Module`or`AttributeTargets.All`.  
  
## See Also  
 <xref:System.AttributeUsageAttribute>   
 <xref:System.AttributeTargets>