---
title: "Conversion from &#39;Date&#39; to &#39;Double&#39; requires calling the &#39;Date.ToOADate&#39; method"
ms.custom: na
ms.date: "10/13/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "bc30532"
  - "vbc30532"
helpviewer_keywords: 
  - "BC30532"
ms.assetid: 8171ce21-e4f6-4e75-b7e8-32baf78a40eb
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
# Conversion from &#39;Date&#39; to &#39;Double&#39; requires calling the &#39;Date.ToOADate&#39; method
You have attempted to cast a `Date` value to a `Double` value, which cannot be done without using the <xref:System.DateTime.ToOADate*?displayProperty=fullName> method.  
  
 **Error ID:** BC30532  
  
### To correct this error  
  
-   Use the <xref:System.DateTime.ToOADate*?displayProperty=fullName> method to convert the value.  
  
## See Also  
 [Type Conversions in Visual Basic](../Topic/Type%20Conversions%20in%20Visual%20Basic.md)