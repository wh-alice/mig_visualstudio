---
title: "XML comment tag &#39;returns&#39; is not permitted on a &#39;WriteOnly&#39; Property | Microsoft Docs"
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
  - "vbc42313"
  - "bc42313"
helpviewer_keywords: 
  - "BC42313"
ms.assetid: 43dca605-187e-4b0b-b29f-5cc4dcdc5f9f
caps.latest.revision: 12
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
# XML comment tag &#39;returns&#39; is not permitted on a &#39;WriteOnly&#39; Property
XML comment tag 'returns' is not permitted on a 'WriteOnly' Property. XML comment will be ignored.  
  
 An XML comment for a write-only property declaration cannot contain a \<returns> tag.  
  
 **Error ID:** BC42313  
  
### To correct this error  
  
-   Remove the unsupported \<returns> tag.  
  
## See Also  
 [\<returns>](http://msdn.microsoft.com/en-us/Library/a03a6469-d907-425d-882f-083187950e7e)   
 [XML Comment Tags](/dotnet/visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments)   
 [Documenting Your Code with XML](/dotnet/visual-basic/programming-guide/program-structure/documenting-your-code-with-xml)   
 [Property Statement](/dotnet/visual-basic/language-reference/statements/property-statement)