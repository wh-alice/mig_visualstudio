---
title: "How to: Debug the OnStart Method"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "FSharp"
  - "VB"
  - "CSharp"
  - "C++"
helpviewer_keywords: 
  - "OnStart method"
  - "debugging [Visual Studio], Windows services"
  - "debugging managed code, OnStart method"
  - "debugging Windows Services applications, OnStart method"
  - "Windows Service applications, debugging"
ms.assetid: b06b5d65-424b-490f-bf58-97583cd7006a
caps.latest.revision: 16
ms.author: "mikejo"
manager: "ghogen"
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
# How to: Debug the OnStart Method
You can debug a Windows service by starting the service and attaching the debugger to the service process. For more information, see [How to: Debug Windows Service Applications](../Topic/How%20to:%20Debug%20Windows%20Service%20Applications.md). However, to debug the <xref:System.ServiceProcess.ServiceBase.OnStart*?displayProperty=fullName> method of a Windows service, you must launch the debugger from inside the method.  
  
1.  Add a call to <xref:System.Diagnostics.Debugger.Launch*> at the beginning of the `OnStart()`method.  
  
    ```c#  
    protected override void OnStart(string[] args)  
    {  
        System.Diagnostics.Debugger.Launch();  
     }  
    ```  
  
2.  Start the service (you can use `net start`, or start it in the **Services** window).  
  
     You should see a dialog box like the following:  
  
     ![OnStartDebug](../debugger/media/onstartdebug.png "OnStartDebug")  
  
3.  Select **Yes, debug \<service name>.**  
  
4.  In the Just-In-Time Debugger window, select the version of Visual Studio you want to use for debugging.  
  
     ![JustInTimeDebugger](../debugger/media/justintimedebugger.png "JustInTimeDebugger")  
  
5.  A new instance of Visual Studio starts, and execution is stopped at the `Debugger.Launch()` method.  
  
## See Also  
 [Debugger Security](../debugger/debugger-security.md)   
 [Debugging Managed Code](../debugger/debugging-managed-code.md)