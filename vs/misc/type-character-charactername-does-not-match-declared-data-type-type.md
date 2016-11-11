---
title: "Type character &#39;&lt;charactername&gt;&#39; does not match declared data type &#39;&lt;type&gt;&#39; | Microsoft Docs"
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
  - "vbc30277"
  - "bc30277"
helpviewer_keywords: 
  - "BC30277"
ms.assetid: 9808f57e-a46c-43f9-b5e7-275794627763
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
# Type character &#39;&lt;charactername&gt;&#39; does not match declared data type &#39;&lt;type&gt;&#39;
A variable is declared with one data type but referred to with a type character representing an incompatible data type, for example `K$ = 10` when `K` is declared `Integer`.  
  
 **Error ID:** BC30277  
  
### To correct this error  
  
-   Change the declared data type of the variable, or change or remove the type character in the reference.  
  
## See Also  
 [Type Characters](/dotnet/visual-basic/programming-guide/language-features/data-types/type-characters)