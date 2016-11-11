---
title: "GPU Activity Graph | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vs.cv.cpu.graph.gpu"
ms.assetid: d7c769af-95fb-49a3-b5ab-deafecee46fa
caps.latest.revision: 9
author: "mikejo5000"
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
# GPU Activity Graph
The GPU Activity graph in the Concurrency Visualizer displays the level of DirectX activity on the system as measured by the number of DirectX engines that are in use over time.  The graph doesn't show which specific engines were used.  An engine is considered to be in use if it is processing any GPU work.  
  
## GPU Activity Graph Colors  
 Green indicates the consumption of DirectX Engines by the current process.  
  
 Light gray indicates the consumption of DirectX Engines by other processes on the system. To reduce the consumption of DirectX engines by other processes, reduce the number of other processes running on the system.  
  
 White indicates the availability of unused DirectX engines on the system. Those engines are available for your process if you can find more opportunities to exploit them. Some engines can only be used for specific kinds of tasks.  
  
## See Also  
 [Utilization View](../profiling/utilization-view.md)