---
title: "Unscheduled Fiber | Microsoft Docs"
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
  - "bc30948"
  - "vbc30948"
helpviewer_keywords: 
  - "BC30948"
ms.assetid: 982bf6d2-ce62-4451-8a23-82dacf8ee100
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
# Unscheduled Fiber
The debugger cannot evaluate an expression because it is in a logical fiber that is not scheduled on a physical thread. This can happen if the process is running on a SQL server using fibers.  
  
 A fiber consists of a stack and a register context, and it can run on any thread. A fiber can be swapped out of a thread and restarted later on a different thread.  
  
 **Error ID:** BC30948  
  
### To correct this error  
  
-   Make sure that fiber is scheduled on a physical thread.  
  
## See Also  
 [Debugging SQL](http://msdn.microsoft.com/en-us/f27c17e6-1d90-49f2-9fc0-d02e6a27f109)   
 [Debugging in Visual Studio](../debugger/debugging-in-visual-studio.md)