---
title: "ParamArray parameters must be declared &#39;ByVal&#39; | Microsoft Docs"
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
  - "vbc30667"
  - "bc30667"
helpviewer_keywords: 
  - "BC30667"
ms.assetid: 583e231f-a4c9-47aa-ae37-7bac43b0b318
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
# ParamArray parameters must be declared &#39;ByVal&#39;
`ParamArray` parameters cannot use the `ByRef` modifier.  
  
 **Error ID:** BC30667  
  
### To correct this error  
  
-   Declare `ParamArray` parameters using the `ByVal` modifier.  
  
## See Also  
 [ParamArray](/dotnet/visual-basic/language-reference/modifiers/paramarray)   
 [ByRef](/dotnet/visual-basic/language-reference/modifiers/byref)   
 [ByVal](/dotnet/visual-basic/language-reference/modifiers/byval)