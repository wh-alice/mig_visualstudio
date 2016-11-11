---
title: "&#39;Get&#39; statements are no longer supported | Microsoft Docs"
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
  - "vbc30829"
  - "bc30829"
helpviewer_keywords: 
  - "BC30829"
ms.assetid: 8d798357-7efb-4423-9808-8b20777b97ba
caps.latest.revision: 9
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
# &#39;Get&#39; statements are no longer supported
`Get` statements are no longer supported. File I/O functionality is available in the `Microsoft.VisualBasic` namespace.  
  
 `Get` is not supported for file operations, and can only be used in property procedure syntax.  
  
 **Error ID:** BC30829  
  
### To correct this error  
  
1.  Perform file operations using the members of `System.IO`, `FileSystemObject`, and [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] run-time functions.  
  
## See Also  
 [Processing Drives, Directories, and Files](/dotnet/visual-basic/developing-apps/programming/drives-directories-files/index)   
 [Get Statement](/dotnet/visual-basic/language-reference/statements/get-statement)   
 [File Access with Visual Basic](/dotnet/visual-basic/developing-apps/programming/drives-directories-files/file-access)