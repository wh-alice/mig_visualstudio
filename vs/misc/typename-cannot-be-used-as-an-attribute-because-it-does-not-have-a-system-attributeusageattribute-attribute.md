---
title: "&#39;&lt;typename&gt;&#39; cannot be used as an attribute because it does not have a &#39;System.AttributeUsageAttribute&#39; attribute | Microsoft Docs"
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
  - "vbc31505"
  - "bc31505"
helpviewer_keywords: 
  - "BC31505"
ms.assetid: 7dd84c9d-6711-4dab-afc6-1fe4dee78051
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
# &#39;&lt;typename&gt;&#39; cannot be used as an attribute because it does not have a &#39;System.AttributeUsageAttribute&#39; attribute
An attempt was made to use an attribute that was declared without the `System.AttributeUsageAttribute` to define its usage.  
  
 **Error ID:** BC31505  
  
### To correct this error  
  
1.  Custom attributes must be classes derived from`System.Attribute` that have the `AttributeUsageAttribute` attribute applied.  
  
## See Also  
 <xref:System.AttributeUsageAttribute>   
 [NOT IN BUILD: Custom Attributes in Visual Basic](http://msdn.microsoft.com/en-us/d72d8a5c-8f64-4614-b15b-cad66845d047)