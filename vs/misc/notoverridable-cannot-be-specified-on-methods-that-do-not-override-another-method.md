---
title: "&#39;NotOverridable&#39; cannot be specified on methods that do not override another method | Microsoft Docs"
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
  - "vbc31088"
  - "bc31088"
helpviewer_keywords: 
  - "BC31088"
ms.assetid: 0241197c-51fa-48b8-9a2a-4205d25641d3
caps.latest.revision: 9
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
# &#39;NotOverridable&#39; cannot be specified on methods that do not override another method
Properties and methods are `NotOverridable` by default. The `NotOverridable` modifier can only be used on methods that override another property or method.  
  
 **Error ID:** BC31088  
  
### To correct this error  
  
-   Remove the `NotOverridable` modifier from properties and methods that do not override another member.  
  
## See Also  
 [Overrides](/dotnet/visual-basic/language-reference/modifiers/overrides)   
 [Overloads](/dotnet/visual-basic/language-reference/modifiers/overloads)   
 [NotOverridable](/dotnet/visual-basic/language-reference/modifiers/notoverridable)   
 [Overridable](/dotnet/visual-basic/language-reference/modifiers/overridable)