---
title: "Option -win32manifest ignored | hehe"
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
  - "vbc2034"
  - "bc2034"
helpviewer_keywords: 
  - "BC2034"
ms.assetid: 8009553a-f6ba-4d2b-8ddd-8a9357bc928e
caps.latest.revision: 5
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
# Option /win32manifest ignored
Option /win32manifest ignored. It can be specified only when the target is an assembly.  
  
 The Visual Basic compiler has been passed the `/win32manifest` compiler option when the `/target` option is set to `module`.  
  
 **Error ID:** BC2034  
  
### To correct this error  
  
1.  Remove the `/win32manifest` compiler option or set the `/target` option to `exe`, `winexe`, or `library`.  
  
## See Also  
 [/target (Visual Basic)](../Topic/-target%20\(Visual%20Basic\).md)   
 [/win32manifest (Visual Basic)](../Topic/-win32manifest%20\(Visual%20Basic\).md)   
 [Visual Basic Command-Line Compiler](../Topic/Visual%20Basic%20Command-Line%20Compiler.md)