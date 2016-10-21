---
title: "Collecting Concurrency Data for a Service by Using the Profiler Command Line"
ms.custom: ""
ms.date: "10/20/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 275aacba-b2af-4d34-8931-ee30d777a256
caps.latest.revision: 13
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
# Collecting Concurrency Data for a Service by Using the Profiler Command Line
The concurrency method of [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] Profiling Tools enables you to collect resource contention data and thread activity data that shows you CPU utilization, thread contention, thread migration, synchronization delays, areas of overlapped IO, and other system events.  
  
> [!NOTE]
>  Enhanced security features in Windows 8 and Windows Server 2012 required significant changes in the way the Visual Studio profiler collects data on these platforms. Windows Store apps also require new collection techniques. See [Performance Tools on Windows 8 and Windows Server 2012 applications](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).  
  
## Common Tasks  
  
|Task|Related Content|  
|----------|---------------------|  
|**Attach to a running .NET service**|-   [How to: Attach the Profiler to a .NET Service to Collect Concurrency Data](../profiling/ffbdfe37-8325-44be-bd36-2c8aab2dec7b.md)|  
|**Add tier-interaction data**|-   [Collecting tier interaction data](../profiling/adding-tier-interaction-data-from-the-command-line.md)|  
|**Attach to a running C/C++ service**|-   [How to: Attach the Profiler to a Native Service to Collect Concurrency Data](../profiling/283a1ee1-b43e-4daf-95ae-1311925a42a8.md)|  
  
## Related Tasks  
  
### Profiling Windows Services  
  
|Task|Related Content|  
|----------|---------------------|  
|**Profile by using the sampling method**|-   [Collecting Application Statistics Using Sampling](../profiling/07840ab2-3a92-4744-ac87-48b19e0ceecd.md)|  
|**Profile by using the instrumentation method**|-   [Collecting Detailed Timing Data Using Instrumentation](../profiling/6116e1df-ed3e-4b0d-ac7f-22f7d7ac00ea.md)|  
|**Profile.NET memory allocation and garbage collection**|-   [Collecting .NET Memory Data](../profiling/b1361333-8a09-4a65-87a9-4ac94ceb2d9f.md)|  
  
### Profiling Concurrency Data  
  
|Task|Related Content|  
|----------|---------------------|  
|**Profile stand-alone applications**|-   [Collecting Concurrency Data](../profiling/0a2c6d8a-50b3-48aa-b617-9137b049d21e.md)|  
|**Profile ASP.NET Web applications**|-   [Collecting Concurrency Data](../profiling/0ba431c1-9eaf-4af9-8ce0-669c0835cdc2.md)|  
  
### Analyzing Concurrency Data Views and Reports  
 [Resource Contention Data Views](../profiling/resource-contention-data-views.md)  
  
 [Concurrency Visualizer](../profiling/concurrency-visualizer.md)  
  
## Reference  
 [Command-Line Profiling Tools Reference](../profiling/command-line-profiling-tools-reference.md)