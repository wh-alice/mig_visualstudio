---
title: "GPU Activity (This Process)"
ms.custom: ""
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vs.cv.threads.timeline.gpuexecution"
  - "vs.cv.threads.timeline.gpuactivity"
ms.assetid: 0956edbf-9bcd-4afe-9287-fda628648ca0
caps.latest.revision: 5
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
# GPU Activity (This Process)
The **GPU Activity (This Process)** segments in the Threads view in the Concurrency Visualizer represent times when the GPU was processing requests on behalf of the current process. These requests are sent to the GPU as direct memory access (DMA) packets. The length of a segment represents the time that the GPU was processing a DMA packet on behalf of the current process.  
  
 When you select the GPU activity segment, the report on the **Current** tab displays information about the DMA packet that was processed. This information includes the amount of time that the packet waited in the hardware queue that's associated with the DirectX engine, the process that submitted the packet, and the time that was required to process the packet. A process other than the current process may have physically submitted the DMA packet to the GPU. The Concurrency Visualizer can detect when another process submitted work to the GPU on behalf of the current process.