---
title: "AutoMark | Microsoft Docs"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: c4de965e-0364-4f78-9936-1f509e85df74
caps.latest.revision: 9
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
# AutoMark
The **AutoMark** option specifies the number of milliseconds between the collection of Windows software performance counter events. Windows performance counters are specified in the **WinCounter** option.  
  
 Only one **AutoMark** option can be specified on the command line. Note that the **WinCounter** sampling interval specified by **AutoMark** is independent of the main sampling interval.  
  
## Syntax  
  
```  
VSPerfCmd.exe /Start:Method /WinCounter:Path /AutoMark:Milliseconds  
```  
  
#### Parameters  
 `Milliseconds`  
 Specifies the number of milliseconds between collections of Windows performance counter events.  
  
## Required Options  
 **WinCounter:** `Path`  
 Specifies the Windows performance counter to collect. When you are using the instrumentation method, multiple Windows counters can be specified. When you are using the sampling method, only one software counter can be specified. The **WinCounter** option must be specified in a command line that contains the **Start** option.  
  
## Example  
 In this example, a sampling interval of 1000 milliseconds is set for two Windows performance counters.  
  
```  
VSPerfCmd.exe /Start:Trace /Output:TestApp.exe.vsp /WinCounter:"\Process(*)\% Processor Time" /WinCounter:"\ASP.NET\Pages/sec" /AutoMark:1000  
VSPerfCmd.exe /Launch:TestApp.exe  
```  
  
## See Also  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [Profiling Stand-Alone Applications](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [Profiling ASP.NET Web Applications](../profiling/command-line-profiling-of-asp.net-web-applications.md)   
 [Profiling Services](../profiling/command-line-profiling-of-services.md)