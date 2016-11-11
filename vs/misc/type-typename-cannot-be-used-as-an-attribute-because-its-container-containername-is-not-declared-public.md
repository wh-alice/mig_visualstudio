---
title: "Type &#39;&lt;typename&gt;&#39; cannot be used as an attribute because its container &#39;&lt;containername&gt;&#39; is not declared &#39;Public&#39; | Microsoft Docs"
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
  - "bc31517"
  - "vbc31517"
helpviewer_keywords: 
  - "BC31517"
ms.assetid: 3d1a8f41-8652-4e37-a6bd-40b0ad306c6f
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
# Type &#39;&lt;typename&gt;&#39; cannot be used as an attribute because its container &#39;&lt;containername&gt;&#39; is not declared &#39;Public&#39;
The class or module where this attribute is defined is not declared using the `Public` modifier. Classes and modules that do not specify an access modifier are declared as `Friend` by default.  
  
 **Error ID:** BC31517  
  
### To correct this error  
  
1.  Add the `Public` modifier to the class or module where this attribute is defined.  
  
## See Also  
 [Public](/dotnet/visual-basic/language-reference/modifiers/public)