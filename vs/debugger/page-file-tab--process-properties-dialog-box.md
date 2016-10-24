---
title: "Page File Tab, Process Properties Dialog Box | testtitle"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "Process properties for Windows NT"
ms.assetid: daf41a06-8a55-48f6-95f5-49a8416bd308
caps.latest.revision: 4
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
# Page File Tab, Process Properties Dialog Box
Use the **Page File** tab to examine the paging file of a process. To display the [Process Properties Dialog Box](../debugger/process-properties-dialog-box.md), move the focus to a [Processes View](../debugger/processes-view.md) window. Select any process node in the tree, then choose **Properties** from the **View** menu.  
  
 The following settings are available on the **Page File** tab:  
  
|Entry|Description|  
|-----------|-----------------|  
|**Page File Bytes**|The current number of pages that this process is using in the paging file. The paging file stores pages of data used by the process but not contained in other files. The paging file is used by all processes, and lack of space in the paging file can cause errors while other processes are running.|  
|**Peak Page File Bytes**|The maximum number of pages that this process has used in the paging file.|  
|**Page Faults**|The number of Page Faults by the threads executing in this process. A page fault occurs when a thread refers to a virtual memory page that is not in its working set in main memory. Thus, the page will not be retrieved from disk if it is on the standby list and hence already in main memory, or if it is being used by another process with which the page is shared.|