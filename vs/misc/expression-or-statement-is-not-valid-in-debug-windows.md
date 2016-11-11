---
title: "Expression or statement is not valid in debug windows | Microsoft Docs"
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
  - "bc30706"
  - "vbc30706"
helpviewer_keywords: 
  - "BC30706"
ms.assetid: 229bb582-d962-4385-97e7-120dcf5d8991
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
# Expression or statement is not valid in debug windows
`Try...Catch...Finally` statements cannot be used in the debugging context.  
  
 **Error ID:** BC30706  
  
### To correct this error  
  
1.  Remove `Try...Catch...Finally` statements from debugging code.  
  
## See Also  
 [Try...Catch...Finally Statement](/dotnet/visual-basic/language-reference/statements/try-catch-finally-statement)   
 [Debugging in Visual Studio](../debugger/debugging-in-visual-studio.md)