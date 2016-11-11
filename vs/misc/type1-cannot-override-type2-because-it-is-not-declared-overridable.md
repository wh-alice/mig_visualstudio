---
title: "&#39;&lt;type1&gt;&#39; cannot override &lt;type2&gt; because it is not declared &#39;Overridable&#39; | Microsoft Docs"
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
  - "bc31086"
  - "vbc31086"
helpviewer_keywords: 
  - "BC31086"
ms.assetid: ce071994-2e32-4460-a65d-f48f914386c6
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
# &#39;&lt;type1&gt;&#39; cannot override &lt;type2&gt; because it is not declared &#39;Overridable&#39;
A member in a derived class overrides a base class member that is not marked with the `Overridable` modifier.  
  
 **Error ID:** BC31086  
  
### To correct this error  
  
1.  Add the `Overridable` modifier to the overridden member in the base class.  
  
2.  Use the `Shadows` keyword to shadow the item in the base class.  
  
## See Also  
 [Overridable](/dotnet/visual-basic/language-reference/modifiers/overridable)   
 [Overrides](/dotnet/visual-basic/language-reference/modifiers/overrides)   
 [Shadows](/dotnet/visual-basic/language-reference/modifiers/shadows)