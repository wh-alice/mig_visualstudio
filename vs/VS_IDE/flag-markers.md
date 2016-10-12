---
title: "Flag Markers"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "vs.cv.markers.flag"
ms.assetid: f3ec919e-63e5-484b-adbf-8f0e79342e75
caps.latest.revision: 9
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
# Flag Markers
A flag marker represents something that occurred at an instant in time in an app. A flag can represent many kinds of application events. For example, a flag could show when a particular work item was scheduled or when an exception was thrown. Runtimes such as the Task Parallel Library can also generate flags.  
  
## Flag Importance  
 Flags are displayed in different sizes depending on their importance. Like any marker, the importance can be low, normal, high, or critical.  This illustration shows the appearance of markers by importance level:  
  
 ![Low, Normal, High, and Critical importance markers](../VS_IDE/media/cvmarkerimportance.png "CVMarkerImportance")  
Markers showing flag importance  
  
## Flag Category  
 A flag is displayed in one of five different colors depending on its category. The colors are reused if there are more than five categories. You cannot choose the color. Like any marker, the category can be any integer. The next illustration shows the colors for the first five categories.  
  
 ![Five colors of category markers](../VS_IDE/media/cvmarkercategory.png "CVMarkerCategory")  
Markers showing categories  
  
## Alerts  
 An alert is a red-colored flag that represents a critical application event, such as an exception.  Here's an alert:  
  
 ![The Concurrency Visualizer Alert Marker](../VS_IDE/media/cvmarkeralert.png "CVMarkerAlert")  
An alert marker  
  
## Aggregation Flags  
 Sometimes flags occur so close to one another in the Concurrency Visualizer that they can’t be drawn individually. When this occurs, a gray *aggregation flag* that represents the underlying flags is shown. When you rest the pointer on one of these icons, a tooltip displays the number of underlying flags that are represented. To view the flags, zoom in. If you zoom in all the way and still get an aggregation flag, you can view the underlying flags in the [Markers Report](../VS_IDE/markers-report.md).  
  
 Aggregation flags are drawn in different sizes. The size depends on the importance level of the most important flag in the aggregation. The following illustration shows aggregation flags in increasing order of importance.  
  
 ![Aggregate flags showing four levels of importance](../VS_IDE/media/cvmarkeraggregate.png "CVMarkerAggregate")  
Aggregation flags by level of importance  
  
## See Also  
 [Concurrency Visualizer Markers](../VS_IDE/concurrency-visualizer-markers.md)   
 [Concurrency Visualizer SDK](../VS_IDE/concurrency-visualizer-sdk.md)