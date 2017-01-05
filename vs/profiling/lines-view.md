---
title: "Lines View"
ms.custom: ""
ms.date: "12/07/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vs.performance.view.lines"
helpviewer_keywords: 
  - "profiling tools reports, Line view"
  - "profiling tools, Line view"
  - "Lines view"
ms.assetid: 71ec0781-6031-4e17-af09-f50226018437
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
# Lines View
[!INCLUDE[vs2017banner](../code-quality/includes/vs2017banner.md)]

The Lines view is available only for profiler data that was collected by using the sampling method. The view is not available for data that was collected by using instrumentation.  
  
 For sampling profile data, the Lines view identifies the statement in a function that was directly executing when the sample was collected. For .NET memory data, the Lines view identifies the statements that allocate memory.  
  
 In a source file, a statement can span more that one line in a source file, and a single line can include more than one statement.  
  
 A statement is identified by the following:  
  
-   The source file that contains the function statement.  
  
-   The function that contains the statement.  
  
-   The source line at which the statement starts.  
  
-   The character in the source line at which the statement starts.  
  
-   The source line at which the statement ends.  
  
-   The character in the source line at which the statement ends.  
  
## See Also  
 [Lines View](../profiling/lines-view---sampling-data.md)   
 [Lines View - Sampling](../profiling/lines-view---.net-memory-sampling-data.md)   
 [Lines View](../profiling/lines-view---contention-data.md)