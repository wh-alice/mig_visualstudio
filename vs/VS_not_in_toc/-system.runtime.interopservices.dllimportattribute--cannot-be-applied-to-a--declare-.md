---
title: "&#39;System.Runtime.InteropServices.DllImportAttribute&#39; cannot be applied to a &#39;Declare&#39;"
ms.custom: na
ms.date: "10/02/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "bc31523"
  - "vbc31523"
helpviewer_keywords: 
  - "BC31523"
ms.assetid: 04c8a14f-9286-4f9a-aad5-a0555e5f09f4
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
# &#39;System.Runtime.InteropServices.DllImportAttribute&#39; cannot be applied to a &#39;Declare&#39;
The `DllImportAttribute` attribute was applied to a `Declare` function. This attribute can only be used with an empty `Function` or `Sub`.  
  
 **Error ID:** BC31523  
  
### To correct this error  
  
1.  Remove the `DllImportAttribute` attribute from the `Declare` statement.  
  
## See Also  
 \<xref:System.Runtime.InteropServices.DllImportAttribute>   
 [Declare Statement](../Topic/Declare%20Statement.md)