---
title: "Ignoring -noconfig option because it was specified in a response file | testtitle"
ms.custom: ""
ms.date: "10/20/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc2025"
  - "bc2025"
helpviewer_keywords: 
  - "BC2025"
ms.assetid: 87fb393d-e17f-4e50-8d98-d9dfeba30c3e
caps.latest.revision: 10
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
# Ignoring /noconfig option because it was specified in a response file
The `/noconfig` option tells the compiler not to compile with the Vbc.rsp file. However, the compiler processes the Vbc.rsp file before processing any other response files, so the compiler cannot honor the `/noconfig` option in a response file.  
  
 **Error ID:** BC2025  
  
### To correct this error  
  
1.  Remove the `/noconfig` option from the response file.  
  
2.  Specify the `/noconfig` option when invoking the command-line compiler.  
  
## See Also  
 [/noconfig](../Topic/-noconfig.md)   
 [@ (Specify Response File)](../Topic/@%20\(Specify%20Response%20File\)%20\(Visual%20Basic\).md)