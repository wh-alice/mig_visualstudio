---
title: "Empty character setorwas specified."
ms.custom: na
ms.date: "10/01/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "vs.message.VS_E_RE_EMPTYSET"
  - "vs.message.0x800A00DF"
ms.assetid: 27ed2ebe-a492-4bc9-ab33-a09fba6cf1d3
caps.latest.revision: 6
ms.author: "mblome"
manager: "douge"
translation.priority.ht: 
  - "cs-cz"
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "pl-pl"
  - "pt-br"
  - "ru-ru"
  - "tr-tr"
  - "zh-cn"
  - "zh-tw"
---
# Empty character setorwas specified.
This error generally occurs when the regular expressions option has been selected and a string containing incomplete syntax has been specified for the patterns **Set of characters []** or **Character not in set [^]**. For example, `[}`.  
  
### To correct this error  
  
1.  Review the topic Regular Expressions for information on the correct syntax for the pattern and enter the string again.  
  
## See Also  
 [Using Regular Expressions in Visual Studio](../VS_IDE/using-regular-expressions-in-visual-studio.md)   
 [NIB: Find and Replace, Quick Find](assetId:///dad03582-4931-4893-83ba-84b37f5b1600)   
 [Find in Files](../VS_IDE/find-in-files.md)   
 [Finding and Replacing Text](../VS_IDE/finding-and-replacing-text.md)