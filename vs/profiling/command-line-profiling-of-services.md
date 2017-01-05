---
title: "Command-Line Profiling of Services"
ms.custom: ""
ms.date: "12/07/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "profiling toos,services"
  - "profiling services"
ms.assetid: f0d62318-b0e8-49c6-9a30-9f7a6adef2f6
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
# Command-Line Profiling of Services
[!INCLUDE[vs2017banner](../code-quality/includes/vs2017banner.md)]

This section describes the procedures and options for collecting performance data for Windows services by using [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] Profiling Tools from the command line.  
  
> [!NOTE]
>  Enhanced security features in Windows 8 and Windows Server 2012 required significant changes in the way the Visual Studio profiler collects data on these platforms. Windows Store apps also require new collection techniques. See [Performance Tools on Windows 8 and Windows Server 2012 applications](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).  
  
## Common Tasks  
  
|Task|Related Content|  
|----------|---------------------|  
|**Collect application statistics:** Use the sampling method to collect performance statistics. Sampling data is useful for analyzing CPU utilization issues and for understanding the general performance characteristics of an application.|-   [Collecting Application Statistics Using Sampling](../profiling/07840ab2-3a92-4744-ac87-48b19e0ceecd.md)|  
|**Collect detailed timing data:** Use the instrumentation method to collect detailed timing information. Instrumentation data is useful for analyzing IO issues and for fine-grained analysis of application scenarios.|-   [Collecting Detailed Timing Data Using Instrumentation](../profiling/6116e1df-ed3e-4b0d-ac7f-22f7d7ac00ea.md)|  
|**Collect .NET memory data:** Use sampling or instrumentation to collect .NET memory allocation data that shows you the size and number of allocated objects. You can also collect object lifetime data that shows you the size and number of objects that are reclaimed in each garbage collection generation.|-   [Collecting .NET Memory Data](../profiling/b1361333-8a09-4a65-87a9-4ac94ceb2d9f.md)|  
|**Collect concurrency data:** Use the concurrency method to collect resource contention data and thread activity data that shows you CPU utilization, thread contention, thread migration, synchronization delays, areas of overlapped IO, and other system events.|-   [Collecting Concurrency Data](../profiling/collecting-concurrency-data-for-a-service-by-using-the-profiler-command-line.md)|  
|**Add tier interaction data:** You can add performance data about synchronous ADO.NET calls that the service made to a Microsoft [!INCLUDE[ssNoVersion](../data-tools/includes/ssnoversion_md.md)] database.|-   [Collecting tier interaction data](../profiling/adding-tier-interaction-data-from-the-command-line.md)|  
  
## Related Tasks  
  
|Task|Related Content|  
|----------|---------------------|  
|**Profile stand-alone (client) applications**|-   [Profiling Stand-Alone Applications](../profiling/command-line-profiling-of-stand-alone-applications.md)|  
|**Profile ASP.NET applications**|-   [Profiling ASP.NET Web Applications](../profiling/command-line-profiling-of-asp.net-web-applications.md)|