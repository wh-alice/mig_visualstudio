---
title: "Methods declared &#39;Overrides&#39; cannot be declared &#39;Overridable&#39; because they are implicitly overridable | Microsoft Docs"
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
  - "bc30730"
  - "vbc30730"
helpviewer_keywords: 
  - "BC30730"
ms.assetid: cc892f81-eb1f-42a9-8f54-eff352adb5dd
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
# Methods declared &#39;Overrides&#39; cannot be declared &#39;Overridable&#39; because they are implicitly overridable
Unlike most methods, methods marked with the `Overrides` modifier are overridable by default.  
  
 **Error ID:** BC30730  
  
### To correct this error  
  
-   Omit the `Overridable` modifier from methods marked with the `Overrides` modifier.  
  
## See Also  
 [Overrides](/dotnet/visual-basic/language-reference/modifiers/overrides)   
 [Overridable](/dotnet/visual-basic/language-reference/modifiers/overridable)