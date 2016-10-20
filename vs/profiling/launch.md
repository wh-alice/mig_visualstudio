---
title: "Launch | Microsoft Docs"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: f81bde5c-3394-4b79-a315-c2f6491689b3
caps.latest.revision: 13
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
# Launch
The **Launch** option starts the profiler using the sampling method and it also starts the specified application.  
  
 To use the **Launch** option, you must specify the **Sample** method in the **Start** option.  
  
## Syntax  
  
```  
VSPerfCmd.exe /Launch:AppName [Options]  
```  
  
#### Parameters  
 `AppName`  
 The name of the application to launch. Full and partial paths from the current directory are supported.  
  
## Valid Options  
 The following VSPerfCmd options can be combined with the **Launch** option on a single command line.  
  
 **Start:** `Method`  
 Initializes the command-line profiler session and sets the specified profiling method.  
  
 **GlobalOn**and **GlobalOff**  
 Resumes (**GlobalOn**) or pauses (**GlobalOff**) profiling, but does not end the profiling session.  
  
 **ProcessOn:** `PID` and **ProcessOff**:`PID`  
 Resumes (**ProcessOn**) or pauses (**ProcessOff**) profiling for the specified process.  
  
 **TargetCLR**  
 Specifies the version of the .NET Framework Common Language Runtime (CLR) to profile when more than one version is loaded in a profiling session. By default, the first loaded version is profiled.  
  
## Exclusive Options  
 The following options can only be used with the **Launch** option.  
  
 **Console**  
 Launches the specified command-line application in a new window.  
  
 **Args:** `ArgList`  
 Specifies the list of arguments to pass to the application.  
  
 **LineOff**  
 Disables the collection of line-level profiling data.  
  
## Sampling Options  
 One of the following sampling interval options can be specified on the **Launch** command line. The default sampling interval is 10,000,000 processor clock cycles.  
  
 **Timer**[**:**`Cycles`]**PF**[**:**`Events`]**Sys**[**:**`Events`]**Counter**[**:**`Name`,`Reload`,`FriendlyName`]**GC**[:**allocation**&#124;**lifetime**]  
 Specifies the number and type of sampling interval.  
  
-   **Timer** - Samples every `Cycles` non-halted processor clock cycles. If `Cycles` is not specified, 10,000,000 cycles are used.  
  
-   **PF** - Samples every `Events` page faults. If `Events` is not specified, 10 page faults.  
  
-   **Sys** - Samples every `Events` calls to the operating system. If `Events` is not specified, 10 system calls are used.  
  
-   **Counter** - Samples every `Reload` number of the CPU performance counter specified by `Name`. Optionally, `FriendlyName` can specify a string to use as the column header in profiler reports.  
  
-   **GC** - Collects .NET memory data. By default (**allocation**), data is collected at every memory allocation event. When the **lifetime** parameter is specified, data is also collected at each garbage collection event.  
  
## Example  
 This example demonstrates the use of **Launch** to start an application.  
  
```  
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp  
VSPerfCmd.exe /Launch:TestApp.exe  
```  
  
## See Also  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [Profiling Stand-Alone Applications](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [Profiling ASP.NET Web Applications](../profiling/command-line-profiling-of-asp.net-web-applications.md)   
 [Profiling Services](../profiling/command-line-profiling-of-services.md)