---
title: "Microsoft Visual Studio Debugger (Exception Thrown) Dialog Box"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "vs.debug.exceptions.thrown"
dev_langs: 
  - "FSharp"
  - "VB"
  - "CSharp"
  - "C++"
helpviewer_keywords: 
  - "Microsoft Visual Studio Debugger (Exception Thrown) dialog box"
  - "exception handling, during debugging"
  - "debugger, exceptions"
  - "throwing exceptions, during debugging"
ms.assetid: 1fe98d10-c8f9-4b39-a920-99169bfd542e
caps.latest.revision: 10
ms.author: "mikejo"
manager: "ghogen"
translation.priority.ht: 
  - "cs-cz"
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "pl-pl"
  - "pt-br"
  - "ru-ru"
  - "tr-tr"
  - "zh-cn"
  - "zh-tw"
---
# Microsoft Visual Studio Debugger (Exception Thrown) Dialog Box
An exception has occurred in your program. This dialog box reports the kind of exception thrown. Your code needs to handle this exception. You can choose between the following options for handling the exception:  
  
 **Break**  
 Allows execution to break into the debugger. The exception handler is not invoked prior to the break. If you continue from the break, the exception handler will be invoked.  
  
 **Continue**  
 Allows execution to continue, giving the exception handler a chance to handle the exception. This option is not available for certain types of exceptions. **Continue** will allow the application to continue. In a native application, it will cause the exception to be rethrown. In a managed application, it will either cause the program to terminate or the exception to be handled by a hosting application.  
  
> [!NOTE]
>  You cannot continue after an unhandled exception in managed code. Choosing **Continue** after an unhandled exception in managed code causes debugging to stop.  
  
 **Ignore**  
 Allows execution to continue without invoking the exception handler. Because the exception handler is not invoked, this can lead to further consequences, including additional exceptions and errors. This option is not available for certain types of exceptions.  
  
## See Also  
 [Managing Exceptions with the Debugger](../debugger/managing-exceptions-with-the-debugger.md)   
 [Best Practices for Exceptions](../Topic/Best%20Practices%20for%20Exceptions.md)   
 [Exception Handling](../Topic/Exception%20Handling%20%20\(C++%20Component%20Extensions\).md)