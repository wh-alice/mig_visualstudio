---
title: "MSBuild Error MSB3021 | Microsoft Docs"
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
  - "MSBuild.Copy.Error"
helpviewer_keywords: 
  - "MSB3021"
ms.assetid: 8cb3a860-6916-4406-b5c7-b1106b44b92a
caps.latest.revision: 10
ms.author: "mblome"
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
# MSBuild Error MSB3021
**Unable to copy file "'\<file>'" to file "'\<file>'". '\<error>'**  
  
 The `Copy` task cannot copy the specified file.  
  
### To correct this error  
  
-   Check to see if the target file is locked (in use) by another application. Be sure you have permission to read the source file and to write the target file to the target folder. If the destination file path is extremely long, you may need to copy to a different location.  
  
## See Also  
 [Copy Task](../reference/copy-task.md)   
 [Tasks](../reference/msbuild-tasks.md)