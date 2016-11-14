---
title: "Security Issues | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "security [Debugging SDK]"
  - "debugging [Debugging SDK], security"
ms.assetid: d6ffff0a-afb4-4f38-86d8-476c881c4e4b
caps.latest.revision: 12
ms.author: "gregvanl"
manager: "ghogen"
translation.priority.mt: 
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
# Security Issues
To debug a program using Visual Studio, the only permissions needed are the same ones a developer needs to run the program. This includes remote debugging for most situations (some situations involving other services, such as the Internet Information Service, may require a higher level of permissions).  
  
 While Visual Studio is running, the process debug manager (PDM) tracks debug processes on the local machine. Remotely, a program called msvsmon.exe is started by the developer to handle remote debugging and make the PDM available. (Note that msvsmon.exe is not a service and must be started manually to enable remote debugging on that machine.) When Visual Studio (or msvsmon.exe) is not running, no processes are tracked for debugging.  
  
 This means that a developer can debug programs he or she started with no special permissions. The developer can even debug processes started by someone else if that other person is a member of the same security group. And to enable remote debugging, it is necessary only to copy the necessary files to the remote machine and start msvsmon.exe (see [Set Up the Remote Tools on the Device](http://msdn.microsoft.com/en-us/Library/90f45630-0d26-4698-8c1f-63f85a12db9c) for more details).  
  
## See Also  
 [Debugging Tasks](../../extensibility/debugger/debugging-tasks.md)   
 [Process Debug Manager](../../extensibility/debugger/process-debug-manager.md)   
 [Set Up the Remote Tools on the Device](http://msdn.microsoft.com/en-us/Library/90f45630-0d26-4698-8c1f-63f85a12db9c)