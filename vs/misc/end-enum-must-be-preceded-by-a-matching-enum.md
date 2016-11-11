---
title: "&#39;End Enum&#39; must be preceded by a matching &#39;Enum&#39; | Microsoft Docs"
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
  - "bc30184"
  - "vbc30184"
helpviewer_keywords: 
  - "BC30184"
ms.assetid: b7f5ebf0-10c8-4320-8caf-dffc24ae8a71
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
# &#39;End Enum&#39; must be preceded by a matching &#39;Enum&#39;
An `End Enum` statement occurs without a corresponding `Enum` statement. `End Enum` must be preceded by a corresponding `Enum` statement.  
  
 **Error ID:** BC30184  
  
### To correct this error  
  
1.  Ensure that a preceding `Enum` statement is not misspelled or otherwise invalid.  
  
2.  Ensure that the `Enum` members are correctly formatted.  
  
## See Also  
 [Enum Statement](/dotnet/visual-basic/language-reference/statements/enum-statement)