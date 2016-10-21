---
title: "Argument BasePath must be a path to a folder | hehe"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: b180ce60-ad57-41a6-a313-491d86d84cc7
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
# Argument BasePath must be a path to a folder
The argument `BasePath` must consist of a path to a folder. You may be parsing a string incorrectly and supplying a value that is not recognized as a valid path.  
  
### To correct this error  
  
-   Check the value you are supplying for `BasePath` to make sure it is a valid path to a folder.  
  
## See Also  
 <xref:System.CodeDom.Compiler.TempFileCollection.BasePath*>   
 <xref:System.Resources.ResXResourceWriter.BasePath*>   
 <xref:System.Resources.ResXResourceReader.BasePath*>   
 [How to: Parse File Paths](../Topic/How%20to:%20Parse%20File%20Paths%20in%20Visual%20Basic.md)