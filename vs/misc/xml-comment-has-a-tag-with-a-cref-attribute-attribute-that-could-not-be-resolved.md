---
title: "XML comment has a tag with a &#39;cref&#39; attribute &#39;&lt;attribute&gt;&#39; that could not be resolved | Microsoft Docs"
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
  - "bc42309"
  - "vbc42309"
helpviewer_keywords: 
  - "BC42309"
ms.assetid: c9f3cfa5-565f-48bf-8616-cfb25d24f89e
caps.latest.revision: 19
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
# XML comment has a tag with a &#39;cref&#39; attribute &#39;&lt;attribute&gt;&#39; that could not be resolved
XML comment has a tag with a 'cref' attribute \<attribute> that could not be resolved. XML comment will be ignored.  
  
 Tags can have a `cref` attribute that designates a link to another element of the XML by specifying the relative name of the identifier. At compile time, the compiler replaces the value with the qualified XML identifier for the value pointed at by the user. The compiler uses its normal resolution rules for finding the type or member.  
  
 **Error ID:** BC42309  
  
### To correct this error  
  
-   Validate the `cref` attribute so that it points to a valid code element.  
  
## See Also  
 [How to: Create XML Documentation](http://msdn.microsoft.com/en-us/Library/27b5b06c-09b9-496a-8245-f9542d846230)   
 [XML Comment Tags](/dotnet/visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments)