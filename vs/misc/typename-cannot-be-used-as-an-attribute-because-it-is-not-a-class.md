---
title: "&#39;&lt;typename&gt;&#39; cannot be used as an attribute because it is not a class | Microsoft Docs"
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
  - "bc31503"
  - "vbc31503"
helpviewer_keywords: 
  - "BC31503"
ms.assetid: 9979f794-5d6d-4cc6-a2ec-303078626c0f
caps.latest.revision: 7
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
# &#39;&lt;typename&gt;&#39; cannot be used as an attribute because it is not a class
An attempt was made to use a type that is not a class as an attribute.  
  
 **Error ID:** BC31503  
  
### To correct this error  
  
1.  Define custom attributes as classes that derive from `System.Attribute`.  
  
## See Also  
 [NOT IN BUILD: Attributes in Visual Basic](http://msdn.microsoft.com/en-us/620bfc0e-4582-4c8b-8432-ebc5c3dccc22)