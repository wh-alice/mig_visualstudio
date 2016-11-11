---
title: "Enums must be declared as an integral type | Microsoft Docs"
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
  - "bc30650"
  - "vbc30650"
helpviewer_keywords: 
  - "BC30650"
ms.assetid: 566aa501-d283-4c1f-b494-3bc5fbe80e04
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
# Enums must be declared as an integral type
The only valid types you can use in enumerations are `SByte`, `Byte`, `Short`, `UShort`, `Integer`, `UInteger`, `Long`, and `ULong`. No other data types can be used.  
  
 **Error ID:** BC30650  
  
### To correct this error  
  
-   Specify a data type of `SByte`, `Byte`, `Short`, `UShort`, `Integer`, `UInteger`, `Long`, or `ULong`.  
  
## See Also  
 [Data Types](/dotnet/visual-basic/language-reference/data-types/data-type-summary)   
 [Enum Statement](/dotnet/visual-basic/language-reference/statements/enum-statement)