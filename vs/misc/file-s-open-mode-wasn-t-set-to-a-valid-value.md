---
title: "File&#39;s open mode wasn&#39;t set to a valid value | Microsoft Docs"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 969541f6-9ff6-4804-ba61-0d17370060ef
caps.latest.revision: 10
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
# File&#39;s open mode wasn&#39;t set to a valid value
The value supplied for the file's open mode was not valid. The following table shows valid values for the <xref:Microsoft.VisualBasic.OpenMode> enumeration.  
  
|Value|Mode|  
|-----------|----------|  
|1|`OpenMode.Input`|  
|2|`OpenMode.Output`|  
|4|`OpenMode.Random`|  
|8|`OpenMode.Append`|  
|32|`OpenMode.Binary`|  
  
### To correct this error  
  
-   Verify the value being supplied for the file's open mode.  
  
## See Also  
 [NOTINBUILD OpenMode Enumeration](http://msdn.microsoft.com/en-us/e995bd42-d11f-455c-88c4-308345172633)   
 [My.Computer.FileSystem Object](../Topic/My.Computer.FileSystem%20Object.md)   
 [Reading from Files](../Topic/Reading%20from%20Files%20in%20Visual%20Basic.md)   
 [Writing to Files](../Topic/Writing%20to%20Files%20in%20Visual%20Basic.md)