---
title: "Command-Line Profiling of Stand-Alone Applications | testtitle"
ms.custom: ""
ms.date: "10/20/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "profillng tools,stand-alone applications"
  - "profling stand-alone applications"
ms.assetid: a47f2bf2-186d-4120-bb79-34e2f3a1ee42
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
# Command-Line Profiling of Stand-Alone Applications
This section describes the procedures and options for collecting performance data for stand-alone (client) applications by using the [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] Profiling Tools from the command line.  
  
## Common Tasks  
  
|Task|Related content|  
|----------|---------------------|  
|**Collect application statistics:** Use the sampling method to collect performance statistics. Sampling data is useful for analyzing CPU utilization issues and for understanding the general performance characteristics of an application.|-   [Collecting Application Statistics Using Sampling](../profiling/be2dbdd0-fc88-45f9-a1d5-bcb4f64e17ad.md)|  
|**Collect detailed timing data:** Use the instrumentation method to collect detailed timing information. Instrumentation data is useful for analyzing I/O issues and for fine-grained analysis of application scenarios.|-   [Collecting Detailed Timing Data Using Instrumentation](../profiling/4017d9d1-d609-4f41-8e4e-976abae746b3.md)|  
|**Collect .NET memory data:** Use sampling or instrumentation to collect .NET memory allocation data that shows you the size and number of allocated objects. You can also collect object lifetime data that shows you the size and number of objects that are reclaimed in each garbage collection generation.|-   [Collecting .NET Framework Memory Data](../profiling/7bce69e2-407c-4342-8516-641586968928.md)|  
|**Collect concurrency data:** Use the concurrency method to collect resource contention data and thread activity data that shows you CPU utilization, thread contention, thread migration, synchronization delays, areas of overlapped I/O, and other system events.|-   [Collecting Concurrency Data](../profiling/0a2c6d8a-50b3-48aa-b617-9137b049d21e.md)|  
|**Add tier-interaction data:** You can add performance data about synchronous ADO.NET calls that the application made to a Microsoft [!INCLUDE[ssNoVersion](../data-tools/includes/ssnoversion_md.md)] database. Adding tier interaction data to a profiling run requires specific procedures with the command line profiling tools.|-   [Collecting tier interaction data](../profiling/adding-tier-interaction-data-from-the-command-line.md)|  
|**Try it out:** Use step-by-step procedures to profile a sample client application by using the sampling or instrumentation method.|-   [Walkthrough: Command-Line Profiling Using Sampling](../profiling/walkthrough--command-line-profiling-using-sampling.md)<br />-   [Walkthrough: Command-Line Profiling Using Instrumentation](../profiling/walkthrough--command-line-profiling-using-instrumentation.md)|  
  
## Related Tasks  
  
|Task|Related Content|  
|----------|---------------------|  
|**Profile ASP.NET applications**|-   [Profiling ASP.NET Web Applications](../profiling/command-line-profiling-of-asp.net-web-applications.md)|  
|**Profile services**|-   [Profiling Services](../profiling/command-line-profiling-of-services.md)|