---
title: "The type &#39;&lt;typename&gt;&#39; cannot be an array element type, return type, field type, generics argument type, &#39;ByRef&#39; parameter type or the type of an expression converted to &#39;Object&#39; or &#39;ValueType&#39; | Microsoft Docs"
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
  - "vbc31396"
  - "BC31396"
helpviewer_keywords: 
  - "BC31396"
ms.assetid: 56998a2c-a705-482e-87ee-5eff707f8a48
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
# The type &#39;&lt;typename&gt;&#39; cannot be an array element type, return type, field type, generics argument type, &#39;ByRef&#39; parameter type or the type of an expression converted to &#39;Object&#39; or &#39;ValueType&#39;
An expression declares a variable, procedure parameter, type parameter, function return, or array to be of a restricted type.  
  
 The common language runtime (CLR) exposes certain types solely for special language support, and they should not be used as data types in your application. These types include the <xref:System.ArgIterator>, <xref:System.RuntimeArgumentHandle>, and <xref:System.TypedReference> structures.  
  
 **Error ID:** BC31396  
  
### To correct this error  
  
-   Do not use the restricted structure as a declared data type.  
  
## See Also  
 <xref:System.ArgIterator>   
 <xref:System.RuntimeArgumentHandle>   
 <xref:System.TypedReference>