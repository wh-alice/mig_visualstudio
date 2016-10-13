---
title: "Performance Rules by ID"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: na
ms.topic: "article"
ms.assetid: 9a1c934c-4798-4df9-a8ef-eb17ef06b6a2
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
# Performance Rules by ID
|Warning|Description|  
|-------------|-----------------|  
|[DA0001: Use StringBuilder for concatenations](../profiling/da0001--use-stringbuilder-for-concatenations.md)|Calls to System.String.Concat are a significant proportion of the profiling data. Consider using the \<xref:System.Text.StringBuilder> class to construct strings from multiple segments.|  
|[DA0002: VSPerfCorProf.dll is missing](../profiling/da0002--vsperfcorprof.dll-is-missing.md)|The profiler could not find VSPerfCorProf.dll during the profiling run. This warning occurs when command-line tools for the collection of profiler data are used without using the VSPerfCLREnv.cmd tool to initialize the necessary environment variables.|  
|[DA0003: Many kernel samples](../profiling/da0003--many-kernel-samples.md)|A significant proportion of the call stack samples collected for the application were executing in kernel mode. Consider profiling your application by using a different profiling method.|  
|[DA0004: High processor usage](../profiling/da0004--high-processor-usage.md)|Processor (CPU) utilization was significantly high in profiling data that was collected using the instrumentation method. Consider using the sampling profiling method when profiling a CPU bound application.|  
|[DA0005: Frequent GC2 collections](../profiling/da0005--frequent-gc2-collections.md)|A high number of .NET memory objects are being reclaimed in generation 2 garbage collection.|  
|[DA0006: Override Equals() for value types](../profiling/da0006--override-equals---for-value-types.md)|Calls to the Equals method or the equality operators of a public value type are a significant proportion of the profiling data. Consider implementing a more efficient method.|  
|[DA0007: Avoid using exceptions for control flow](../profiling/da0007--avoid-using-exceptions-for-control-flow.md)|A high rate of .NET Framework exception handlers were called in the profiling data. Consider using other control flow logic to reduce the number of exceptions that are thrown.|  
|[DA0008: Few samples collected](../profiling/da0008--few-samples-collected.md)|Only a few samples were collected in the profiling run. Consider a longer run or faster sampling rate for more significant results.|  
|[DA0009: High % time in JIT](http://msdn.microsoft.com/b60c1767-515c-41d9-81c2-c70d0b7024fd)|A significant percentage of application execution time was spent in the Just In Time (JIT) compiler.|  
|[DA0010: Expensive GetHashCode](../profiling/da0010--expensive-gethashcode.md)|Calls to the GetHashCode method of the type are a significant proportion of the profiling data or the method allocates memory.|  
|[DA0011: Expensive CompareTo](../profiling/da0011--expensive-compareto.md)|The CompareTo method of the type is expensive or allocates memory.|  
|[DA0012: Significant amount of Reflection](../profiling/da0012--significant-amount-of-reflection.md)|Calls to the System.Reflection methods such as InvokeMember and GetMember or to Type methods such as MemberInvoke are a significant proportion of the profiling data. When you can, consider replacing these methods with early binding to the methods of dependent assemblies.|  
|[DA0013: High usage of String.Split or String.Substring](../profiling/da0013--high-usage-of-string.split-or-string.substring.md)|Calls to the System.String.Split or System.String.Substring methods are a signifiicant portion of the profiling data. Consider using System.String.IndexOf or System.String.IndexOfAny if you are testing for the existence of a substring in a string.|  
|[DA0014: Extremely high rates of paging active memory to disk](../profiling/da0014--extremely-high-rates-of-paging-active-memory-to-disk.md)|System performance data that was collected in the profiling run indicates that an extremely high rate of paging active memory to and from the disk occurred throughout the profiling run. Paging rates at this level usually will impact application performance and responsiveness. Consider reducing memory allocations by revising algorithms. You might also have to consider the memory requirements of your application. running profiling again on a computer that has more memory.|  
|[DA0017: High rates of paging active memory to disk](../profiling/da0017--high-rates-of-paging-active-memory-to-disk.md)|System performance data that was collected in the profiling run indicates that an high rate of paging active memory to and from the disk occurred throughout the profiling run. Paging rates at this level usually will impact application performance and responsiveness. Consider reducing memory allocations by revising algorithms. You might also have to consider the memory requirements of your application. running profiling again on a computer that has more memory.|  
|[DA0018: 32-bit Application running at process managed memory limits](../profiling/da0018--32-bit-application-running-at-process-managed-memory-limits.md)|System data that was collected during the profiling run indicates the .NET Framework memory heaps approached the maximum size the managed heaps can grow to in a 32-bit process. The value reported is the maximum observed value of the heaps while the profiled process being was active. Consider optimizing the use of managed resources by the application.|  
|[DA0021: High rate of Gen 1 garbage collections](../profiling/da0021--high-rate-of-gen-1-garbage-collections.md)|System performance data that was collected during profiling indicate that a significant proportion of the memory for.NET Framework objects was reclaimed in generation 1 of garbage collection compared to generation 0 data collection.|  
|[DA0022: High rate of Gen 2 garbage collections](../profiling/da0022--high-rate-of-gen-2-garbage-collections.md)|System performance data that was collected during profiling indicate that a significant proportion of the memory for.NET Framework objects was reclaimed in generation 2 of garbage collection compared to generation 0 and generation 1 garbage collections.|  
|[DA0023: High GC CPU time](../profiling/da0023--high-gc-cpu-time.md)|System performance data that was collected during profiling indicates that the amount of time spent in garbage collection is significant compared with the total application processing time.|  
|[DA0024: Excessive GC CPU Time](../profiling/da0024--excessive-gc-cpu-time.md)|System performance data that was collected during profiling indicates that the amount of time spent in garbage collection is excessively high compared with the total application processing time.|  
|[DA0026: Excessive kernel CPU time processing](../profiling/da0026--excessive-kernel-cpu-time-processing.md)|The proportion CPU time that was executed in kernel mode exceeded the amount of time spent in user mode. Consider profiling again and sampling the number of system calls (syscalls) to determine the cause of the high kernel mode execution times.|  
|[DA0029: Unsupported CLR Version](../profiling/da0029--unsupported-clr-version.md)|You are trying to profile an application that uses the .NET Framework version 1.1 that is not supported by the Profiling Tools.|  
|[DA0030: Gather Tier Interaction measurements for database projects](../profiling/da0030--gather-tier-interaction-measurements-for-database-projects.md)|Calls to \<xref:System.Data> methods are a significant proportion of the profiling data and you have not collected tier interaction data in the profiling run. Consider profiling again and adding tier interaction data.|  
|[DA0038: High Rate of Lock contentions](../profiling/da0038--high-rate-of-lock-contentions.md)|System performance data that is collected with the profiling data indicates that a significantly high rate of lock contentions occurred during application execution. Consider profiling again using the concurrency profiling method to find the cause of the contentions.|  
|[DA0039: Very High Rate of Lock contentions](../profiling/da0039--very-high-rate-of-lock-contentions.md)|System performance data that is collected with the profiling data indicates that an excessively high rate of lock contentions occurred during application execution. Consider profiling again using the concurrency profiling method to find the cause of the contention.|  
|[DA0501: Average CPU consumption by the Process being profiled.](../profiling/da0501--average-cpu-consumption-by-the-process-being-profiled..md)|This message reports the percentage of time that a processor was busy executing instructions from the application. The reported value is the average over all the measurement intervals in which the process being profiled was active. The value of value can be greater than 100% on a machine with more than one processor.|  
|[DA0502: Maximum CPU consumption by the Process being profiled](../profiling/da0502--maximum-cpu-consumption-by-the-process-being-profiled.md)|This message reports the maximum percentage of time that a processor was busy executing instructions from the application. The reported value is the maximum value reported among all the measurement intervals in which the process being profiled was active. The percentage can be greater than 100% on a machine with more than one processor.|  
|[DA0503: Average Working Set in Bytes for the Process being profiled](../profiling/da0503--average-working-set-in-bytes-for-the-process-being-profiled.md)|This message reports the average amount of physical memory that the process is currently using in bytes (the working set). The process working set represents pages from the process address space that currently reside in physical memory.|  
|[DA0504: Maximum Working Set in Bytes for the Process being profiled](../profiling/da0504--maximum-working-set-in-bytes-for-the-process-being-profiled.md)|This message reports the maximum amount of physical memory that the process is currently using in bytes. The process working set represents pages from the process address space that currently reside in physical memory. This rule reports the maximum value for the process working set while profiling was active.|  
|[DA0505: Average Private Bytes allocated for the Process being profiled](../profiling/da0505--average-private-bytes-allocated-for-the-process-being-profiled.md)|This message reports the average amount of virtual memory that the process has currently allocated in bytes (Private bytes). Private bytes represents virtual memory locations that were allocated by the process that can only be accessed by threads running inside the process.|  
|[DA0506: Maximum Private Bytes allocated for the Process being profiled](../profiling/da0506--maximum-private-bytes-allocated-for-the-process-being-profiled.md)|This message reports the maximum amount of virtual memory that the process has currently allocated in bytes (Private bytes). Private bytes represents virtual memory locations that were allocated by the process that can only be accessed by threads running inside the process.|