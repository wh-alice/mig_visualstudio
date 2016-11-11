---
title: "Attribute constructor has a parameter of type &#39;&lt;type&gt;&#39;, which is not an integral, floating-point, or Enum type or one of Char, String, Boolean, System.Type or 1-dimensional array of these types | Microsoft Docs"
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
  - "bc30045"
  - "vbc30045"
helpviewer_keywords: 
  - "BC30045"
ms.assetid: 16899755-7901-4c56-ae90-54c3532e8319
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
# Attribute constructor has a parameter of type &#39;&lt;type&gt;&#39;, which is not an integral, floating-point, or Enum type or one of Char, String, Boolean, System.Type or 1-dimensional array of these types
A custom attribute definition includes a constructor that specifies an invalid data type for a parameter. Attributes can take only certain data types as parameters, because only those types can be serialized into the metadata for the assembly.  
  
 **Error ID:** BC30045  
  
### To correct this error  
  
1.  Change the data type of the parameter to `Byte`, `Short`, `Integer`, `Long`, `Single`, `Double`, `Char`, `String`, `Boolean`, `System.Type`, or an enumeration type.  
  
## See Also  
 [NOT IN BUILD: Custom Attributes in Visual Basic](http://msdn.microsoft.com/en-us/d72d8a5c-8f64-4614-b15b-cad66845d047)