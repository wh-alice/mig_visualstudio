---
title: "First statement of a method body cannot be on the same line as the method declaration | Microsoft Docs"
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
  - "vbc30040"
  - "bc30040"
helpviewer_keywords: 
  - "BC30040"
ms.assetid: 27df3488-de77-499d-b9a6-08037d540cb0
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
# First statement of a method body cannot be on the same line as the method declaration
A `Function`, `Sub`, `Get`, `Set`, or `Property` statement must be alone on a source code line.  
  
 **Error ID:** BC30040  
  
### To correct this error  
  
1.  Remove any line label preceding the procedure declaration.  
  
2.  Move any statement preceding the procedure declaration to a previous source code line.  
  
3.  Move any statement following the procedure declaration to a subsequent source code line.  
  
## See Also  
 [Procedures](/dotnet/visual-basic/language-reference/procedures/index)   
 [How to: Label Statements](http://msdn.microsoft.com/en-us/Library/38f1ff43-2054-42cb-963b-1998e60c6ed4)