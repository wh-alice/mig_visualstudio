---
title: "Summary View - Resource Contention View"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "Summary view"
ms.assetid: 6da57b83-7b42-4d7c-9aea-8e0a830faf6b
caps.latest.revision: 8
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
# Summary View - Resource Contention View
The Summary view displays information about the events in your application in which a thread or process was suspended while it waited for access to a resource.  
  
 For more information, including a description of the Notification Links and Report lists, see [Summary View](../VS_IDE/summary-view.md).  
  
## Timeline Graph  
 The timeline graph in the Summary view shows the number of contention events of the profiled application over the time that the profiling occurred. You can use the timeline graph to filter the view to a selected time span. For more information, see [How to: Filter Report Views from the Summary Timeline](../VS_IDE/how-to--filter-report-views-from-the-summary-timeline.md).  
  
## Most Contended Resources  
 **Most Contended Resources** lists the resources in the application that caused the most contention events. You can click a resource name to display the Contentions view. The Contentions view provides a detailed timeline of the resource contentions by thread.  
  
 **Most Contended Resources** includes the following data for each resource.  
  
|Column|Description|  
|------------|-----------------|  
|**Name**|The name of the resource.|  
|**Contentions %**|The percentage of all contention events in the profiling data that were contentions over this resource.|  
  
## Most Contended Thread  
 **Most Contended Threads** lists the threads in the application that had the largest number of contention events. You can click a thread name to display the Contentions view that provides a detailed timeline of the resource contentions by the thread.  
  
 **Most Contended Threads** includes the following data for each thread.  
  
|Column|Description|  
|------------|-----------------|  
|**ID**|The thread identifier.|  
|**Name**|The name of the process that owns the thread.|  
|**Contentions %**|The percentage of all contention events in the profiling data that were contentions over this resource.|