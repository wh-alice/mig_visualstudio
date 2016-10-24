---
title: "How to: Attach and Detach Performance Tools to Running Processes | testtitle"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vs.performance.attach"
helpviewer_keywords: 
  - "performance tools, attach process"
  - "profiling tools, detach process"
  - "profiling tools, attach process"
  - "performance tools, detach process"
  - "profiler"
ms.assetid: 56a99c39-e7f6-4f48-ae56-04ab8e022bf7
caps.latest.revision: 30
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
# How to: Attach and Detach Performance Tools to Running Processes
The profiler can be used to attach to or detach from a running process to make sampling and gathering performance data easier. You can use this method to profile a process when you want to avoid gathering data about application load time, or to monitor the performance of a process after it reaches a specific state.  
  
> [!NOTE]
>  The following steps apply to attaching and detaching processes from within the [!INCLUDE[vs_current_short](../code-quality/includes/vs_current_short_md.md)] integrated development environmnent (IDE). For information about how to use command line tools, see [Profiling from the Command-Line](../profiling/using-the-profiling-tools-from-the-command-line.md). For information about how to profile services, see [Profiling Services](../profiling/command-line-profiling-of-services.md).  
  
 The processes that are available to profile depend on the User Access Permissions that are set by an administrator of the computer. A User account may, for example, have permission for any of the following:  
  
-   Advanced profiling features, when the administrator has set the driver and service to start.  
  
-   Sample profiling only (domain users).  
  
-   Deny access to profiling to everybody.  
  
 For more information, see [Profiling and Windows Vista Security](../profiling/profiling-and-windows-vista-security.md) and the ADMIN options in [VSPerfCmd](../profiling/vsperfcmd.md).  
  
### To attach to a running process  
  
1.  On the **Analyze** menu, point to **Profiler** and then click **Attach/Detach**.  
  
     \- or -  
  
     In **Performance Explorer**, right-click the performance session, and then click **Attach/Detach**.  
  
     The **Attach Profiler to Process** dialog box appears.  
  
2.  Click the name of the process that you want to attach to.  
  
3.  Click **Attach**.  
  
### To detach from a running process  
  
1.  On the **Analyze** menu, point to **Profiler** and then click **Attach/Detach**.  
  
     \- or -  
  
     In **Performance Explorer**, right-click the performance session, and then click **Attach/Detach**.  
  
     The **Attach Profiler to Process** dialog box appears.  
  
2.  Click the image name from which you want to detach.  
  
3.  Click **Detach**.  
  
## See Also  
 [Controlling Data Collection](../profiling/controlling-data-collection.md)   
 [Performance Session Overview](../profiling/performance-session-overview.md)   
 [How to: Start and End Performance Data Collection](../profiling/how-to--start-and-end-performance-data-collection.md)   
 [Profiling and Windows Vista Security](../profiling/profiling-and-windows-vista-security.md)   
 [VSPerfCmd](../profiling/vsperfcmd.md)