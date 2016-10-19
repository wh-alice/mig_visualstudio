---
title: "&#39;Option Compare&#39; must be followed by &#39;Text&#39; or &#39;Binary&#39;"
ms.custom: ""
ms.date: "10/13/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc30207"
  - "bc30207"
helpviewer_keywords: 
  - "BC30207"
ms.assetid: e59cf10d-47ce-401d-8474-3b69a3a5f5db
caps.latest.revision: 8
ms.author: "billchi"
manager: "douge"
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
# &#39;Option Compare&#39; must be followed by &#39;Text&#39; or &#39;Binary&#39;
An `Option Compare` statement contains an incorrect setting or no setting. The only settings allowed in `Option Compare` are `Text` and `Binary`.  
  
 **Error ID:** BC30207  
  
### To correct this error  
  
1.  Check to see if the setting specifier is misspelled.  
  
2.  Add either `Text` or `Binary` to the `Option Compare` statement; for example, `Option Compare Text`.  
  
## See Also  
 [Option Compare Statement](../Topic/Option%20Compare%20Statement.md)