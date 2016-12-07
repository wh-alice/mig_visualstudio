---
title: "CA1308: Normalize strings to uppercase"
ms.custom: ""
ms.date: "12/07/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-devops-test"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CA1308"
  - "NormalizeStringsToUppercase"
helpviewer_keywords: 
  - "NormalizeStringsToUppercase"
  - "CA1308"
ms.assetid: 7e9a7457-3f93-4938-ac6f-1389fba8d9cc
caps.latest.revision: 11
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
# CA1308: Normalize strings to uppercase
[!INCLUDE[vs2017banner](../code-quality/includes/vs2017banner.md)]

|||  
|-|-|  
|TypeName|NormalizeStringsToUppercase|  
|CheckId|CA1308|  
|Category|Microsoft.Globalization|  
|Breaking Change|Non-breaking|  
  
## Cause  
 An operation normalizes a string to lowercase.  
  
## Rule Description  
 Strings should be normalized to uppercase. A small group of characters, when they are converted to lowercase, cannot make a round trip. To make a round trip means to convert the characters from one locale to another locale that represents character data differently, and then to accurately retrieve the original characters from the converted characters.  
  
## How to Fix Violations  
 Change operations that convert strings to lowercase so that the strings are converted to uppercase instead. For example, change `String.ToLower(CultureInfo.InvariantCulture)` to `String.ToUpper(CultureInfo.InvariantCulture)`.  
  
## When to Suppress Warnings  
 It is safe to suppress a warning message when you are not making security decision based on the result (for example, when you are displaying it in the UI).  
  
## See Also  
 [Globalization Warnings](../code-quality/globalization-warnings.md)