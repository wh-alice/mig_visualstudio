---
title: "&#39;Microsoft.VisualBasic.ComClassAttribute&#39; and &#39;&lt;attribute&gt;&#39; cannot both be applied to the same class | testtitle"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc32501"
  - "bc32501"
helpviewer_keywords: 
  - "BC32501"
ms.assetid: dc1bf4f1-f030-4df3-aae8-524af9c2fda7
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
# &#39;Microsoft.VisualBasic.ComClassAttribute&#39; and &#39;&lt;attribute&gt;&#39; cannot both be applied to the same class
A `COMClassAttribute` attribute block is used in conjunction with an attribute that does not apply to COM objects. One possible cause is mixing [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] and COM attributes.  
  
 **Error ID:** BC32501  
  
### To correct this error  
  
-   Remove either the `COMClassAttribute` attribute block or the attribute that does not apply to COM.  
  
## See Also  
 [NOT IN BUILD: Attributes Used in Visual Basic](http://msdn.microsoft.com/en-us/22231318-8a40-49af-9245-e0aab723563b)   
 [NOT IN BUILD: Application of Attributes](http://msdn.microsoft.com/en-us/2b1703ed-4437-49b3-bc0b-568094324f47)   
 [ComClassAttribute Class](http://msdn.microsoft.com/en-us/5c2f0835-9210-47dc-bc59-5c1769953574)