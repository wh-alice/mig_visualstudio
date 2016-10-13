---
title: "How to: Create a Profiling Tools ETW Report"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: na
ms.topic: "article"
ms.assetid: bf5547b3-f6c7-4989-9d47-2fe4f1261444
caps.latest.revision: 8
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
# How to: Create a Profiling Tools ETW Report
The Event Tracing for Windows (ETW) report lists the ETW events that are recorded in a performance session of [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] Profiling Tools. ETW data is collected in a binary (.etl) file. For more information about this report, see [Event Tracing for Windows (ETW) Report](../profiling/event-tracing-for-windows--etw--report.md).  
  
> [!NOTE]
>  You cannot display ETW reports in the interface for [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)].  
  
-   For information about how to collect ETW data by using the interface for [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)], see [How to: Collect Event Tracing for Windows (ETW) Data](../profiling/how-to--collect-event-tracing-for-windows--etw--data.md).  
  
-   For information about how to collect ETW data from a command prompt, see [VSPerfCmd](../profiling/vsperfcmd.md) and [Events](../profiling/events--vsperfcmd-.md).  
  
 You generate the ETW report by using the **VSReport/summary:etw** command. The .etl that contains the ETW data must be in the same directory as the profiling data (.vsp or .vsps) file. By default, the report is generated as a comma-separated value (.csv) file. For more information, see [VSPerfReport](../profiling/vsperfreport.md).  
  
### To generate an ETW report  
  
-   In a **Command Prompt** window, type the following command line:  
  
     *ToolsPath* **VSPerfReport** *VSPFile*  **/Summary:ETW [/Xml]**  
  
    |||  
    |-|-|  
    |*ToolsPath*|The path of the Profiling Tools utility. For more information, see [Specifying the Path to Command Line Tools](../profiling/specifying-the-path-to-profiling-tools-command-line-tools.md).|  
    |*VSPFile*|The profiling data (.vsp or .vsps) file. Full and partial paths are accepted.|  
    |Xml|Generates a report that is formatted in XML.|