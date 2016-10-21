---
title: "&#39;:&#39; is not allowed | hehe"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bc31186"
  - "vbc31186"
helpviewer_keywords: 
  - "BC31186"
ms.assetid: 14436245-1b2e-4ca9-a139-bd1d79ed9d72
caps.latest.revision: 6
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
# &#39;:&#39; is not allowed
':' is not allowed. XML qualified names cannot be used in this context.  
  
 An XML literal has been specified with a qualified name in an invalid location, for example, a target in a processing instruction literal.  
  
 **Error ID:** BC31186  
  
### To correct this error  
  
-   Remove the XML literal with the qualified name or move it to a valid location.  
  
     For information about which characters are valid in XML names, see [Extensible Markup Language (XML) 1.0](http://go.microsoft.com/fwlink/?LinkId=73927).  
  
## See Also  
 [XML Literals](../Topic/XML%20Literals%20\(Visual%20Basic\).md)   
 [XML](../Topic/XML%20in%20Visual%20Basic.md)