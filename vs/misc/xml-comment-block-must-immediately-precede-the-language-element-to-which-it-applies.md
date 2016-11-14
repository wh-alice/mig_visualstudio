---
title: "XML comment block must immediately precede the language element to which it applies | Microsoft Docs"
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
  - "vbc42300"
  - "bc42300"
helpviewer_keywords: 
  - "BC42300"
ms.assetid: f9f7d1da-a723-4237-bd78-6db7ed8bc4aa
caps.latest.revision: 16
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
# XML comment block must immediately precede the language element to which it applies
XML comment block must immediately precede the language element to which it applies. XML comment will be ignored.  
  
 This error will also occur if a tag is misplaced or otherwise malformed.  
  
 **Error ID:** BC42300  
  
### To correct this error  
  
1.  Move the comment block to precede the language element to which it applies. Make sure that extraneous characters have not been accidentally inserted before the initial tag.  
  
2.  Make sure the tag is valid.  
  
## See Also  
 [How to: Create XML Documentation](http://msdn.microsoft.com/en-us/Library/27b5b06c-09b9-496a-8245-f9542d846230)   
 [XML Comment Tags](/dotnet/visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments)