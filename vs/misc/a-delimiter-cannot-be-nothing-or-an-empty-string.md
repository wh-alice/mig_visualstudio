---
title: "A delimiter cannot be Nothing or an empty String | Microsoft Docs"
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
  - "vbrTextFieldParser_DelimiterNothing"
ms.assetid: 8885fcd1-c201-409d-9a32-6ff2b13c0c13
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
# A delimiter cannot be Nothing or an empty String
The `TextFieldParser` is unable to read from the file because the `Delimiters` property is set to `Nothing` or is an empty `String` ("").  
  
### To correct this error  
  
-   Supply a valid value for `Delimiters`.  
  
## See Also  
 [TextFieldParser.SetDelimiters Method](http://msdn.microsoft.com/en-us/21fa40ec-5866-4d0e-9fd9-c708a190dcc9)   
 [TextFieldParser.Delimiters Property](http://msdn.microsoft.com/en-us/4eb18f4d-3011-40a9-b668-be93eed0444f)   
 [How to: Read From Comma-Delimited Text Files](../Topic/How%20to:%20Read%20From%20Comma-Delimited%20Text%20Files%20in%20Visual%20Basic.md)   
 [TextFieldParser Object](/dotnet/visual-basic/language-reference/objects/textfieldparser-object)   
 [Parsing Text Files with the TextFieldParser Object](/dotnet/visual-basic/developing-apps/programming/drives-directories-files/parsing-text-files-with-the-textfieldparser-object)