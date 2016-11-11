---
title: "All field widths, except the last element, must be greater than zero | Microsoft Docs"
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
  - "vbrTextFieldParser_FieldWidthsMustPositive"
ms.assetid: 41d8c661-a749-4c89-be56-905c6e7c3c9d
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
# All field widths, except the last element, must be greater than zero
All field widths, except the last element, must be greater than zero. A field width less than or equal to zero in the last element indicates the last field is of variable length.  
  
 The operation has failed because a field width other than the last element is set to zero or less. A field width less than or equal to zero can be used as the last element to indicate that the last field is of variable length, but it cannot be used as any other element.  
  
### To correct this error  
  
-   Set the field width to the correct length.  
  
## See Also  
 [TextFieldParser.SetFieldWidths Method](http://msdn.microsoft.com/en-us/958fed9f-e0f3-4fc5-83b4-386156bdf036)   
 [TextFieldParser.FieldWidths Property](http://msdn.microsoft.com/en-us/c6985360-60c6-494e-89e7-43b6b73f2597)   
 [How to: Read From Fixed-width Text Files](../Topic/How%20to:%20Read%20From%20Fixed-width%20Text%20Files%20in%20Visual%20Basic.md)   
 [TextFieldParser Object](/dotnet/visual-basic/language-reference/objects/textfieldparser-object)