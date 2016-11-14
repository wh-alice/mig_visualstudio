---
title: "Unable to read delimited fields because a double quote is not a legal delimiter when EscapeQuotes is set to True | Microsoft Docs"
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
  - "vbrTextFieldParser_IllegalDelimiter"
ms.assetid: ab8a0c3a-b89c-4617-9e31-7e81f5dca433
caps.latest.revision: 10
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
# Unable to read delimited fields because a double quote is not a legal delimiter when EscapeQuotes is set to True
The `TextFieldParser` cannot read from the file because a quotation mark (") has been supplied as the delimiter and `EscapeQuotes` is set to `True`.  
  
### To correct this error  
  
-   Set `EscapeQuotes` to `False`.  
  
## See Also  
 [TextFieldParser.SetDelimiters Method](http://msdn.microsoft.com/en-us/21fa40ec-5866-4d0e-9fd9-c708a190dcc9)   
 [TextFieldParser.Delimiters Property](http://msdn.microsoft.com/en-us/4eb18f4d-3011-40a9-b668-be93eed0444f)   
 [How to: Read From Comma-Delimited Text Files](http://msdn.microsoft.com/en-us/Library/a8413fe4-0dba-49c8-8692-44fb67a9ec4f)   
 [TextFieldParser Object](/dotnet/visual-basic/language-reference/objects/textfieldparser-object)