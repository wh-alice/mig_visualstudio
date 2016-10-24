---
title: "DA0004: High processor usage | testtitle"
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
  - "vs.performance.rules.DAHighProcessorUsage"
  - "vs.performance.rules.DA0004"
  - "vs.performance.DA0004"
  - "vs.performance.4"
ms.assetid: 2c4fb569-929e-4f1d-8c50-b590ee371351
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
# DA0004: High processor usage
|||  
|-|-|  
|Rule Id|DA0004|  
|Category|Profiling Tools Usage|  
|Profiling methods|Instrumentation<br /><br /> Sampling|  
|Message|Your processor usage is consistently above 75%. Consider using Sampling mode for CPU-bound applications.|  
|Rule type|Information|  
  
 When you profile by using the sampling, .NET memory, or resource contention methods, you must collect at least 10 samples to trigger this rule.  
  
## Cause  
 Processor (CPU) utilization was significantly high in profiling data that was collected using the instrumentation method. Consider using the sampling profiling method when profiling a CPU bound application.  
  
## Rule Description  
 During this profiling run, the processor (or processors) were consistently very busy. High CPU utilization can indicate a CPU-bound application. Instrumented profiles are usually not the most effective way to investigate CPU-usage scenarios. Sampling is usually more effective when you are profiling applications that spend much of their time executing instructions on the processor.  
  
## How to Fix Violations  
 Consider profiling your application again using the sampling method instead of instrumentation method unless you require function timings or you are more interested in understanding input/output than processor bottlenecks.