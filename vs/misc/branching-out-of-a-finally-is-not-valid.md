---
title: "Branching out of a &#39;Finally&#39; is not valid | Microsoft Docs"
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
  - "bc30101"
  - "vbc30101"
helpviewer_keywords: 
  - "BC30101"
ms.assetid: 16a0dc29-3657-4373-b77f-38f3cb80e6c9
caps.latest.revision: 8
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
# Branching out of a &#39;Finally&#39; is not valid
A `GoTo` statement inside a `Finally` block branches outside the block. It is not valid to branch into or out of a `Catch` or `Finally` block.  
  
 **Error ID:** BC30101  
  
### To correct this error  
  
-   Remove the `GoTo` statement, and consider implementing the program logic with decision or loop control structures.  
  
## See Also  
 [Try...Catch...Finally Statement](/dotnet/visual-basic/language-reference/statements/try-catch-finally-statement)   
 [GoTo Statement](/dotnet/visual-basic/language-reference/statements/goto-statement)   
 [Control Flow](/dotnet/visual-basic/programming-guide/language-features/control-flow/index)