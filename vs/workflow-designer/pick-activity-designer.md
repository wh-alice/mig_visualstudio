---
title: "Pick Activity Designer | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.prod: ".net-framework-4.6"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "System.Activities.Statements.Pick.UI"
ms.assetid: 642c0a47-1b47-45de-a19a-ca0606cedd7a
caps.latest.revision: 9
author: "ErikRe"
ms.author: "erikre"
manager: "erikre"
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
# Pick Activity Designer
The <xref:System.Activities.Statements.Pick> activity provides event-based control flow. The activity executes one of several branches in response to a triggering event.  
  
## The Pick Activity  
 A <xref:System.Activities.Statements.Pick> activity contains a collection of <xref:System.Activities.Statements.PickBranch> objects, one of which the <xref:System.Activities.Statements.Pick> activity can execute due to some incoming event that serves as a trigger. In this way [!INCLUDE[wfd1](../workflow-designer/includes/wfd1_md.md)] provides event-based control flow modeling. Each <xref:System.Activities.Statements.PickBranch> contains a <xref:System.Activities.Statements.PickBranch.Trigger%2A> and an <xref:System.Activities.Statements.PickBranch.Action%2A>. At the beginning of a <xref:System.Activities.Statements.Pick> activity’s execution, all the trigger activities of the <xref:System.Activities.Statements.PickBranch> elements are scheduled. When the first activity completes, the corresponding action activity is scheduled, and all other trigger activities are canceled.  
  
### How to use the Pick Activity Designer  
 The **Pick** activity designer can be found in the **Control Flow** category of the **Toolbox**, which is accessed by clicking the **Toolbox** tab on [!INCLUDE[wfd2](../workflow-designer/includes/wfd2_md.md)] (Alternatively, select **Toolbar** from the **View** menu or CTRL+ALT+X.)  
  
 The **Pick** activity designer can be dragged from the **Toolbox** and dropped on to the [!INCLUDE[wfd2](../workflow-designer/includes/wfd2_md.md)] surface wherever activity designers are normally placed, for example inside of a **Sequence** activity designer. After dropping it into [!INCLUDE[wfd2](../workflow-designer/includes/wfd2_md.md)], it creates a <xref:System.Activities.Statements.Pick> activity, which by default contains two empty <xref:System.Activities.Statements.PickBranch> activities as elements with display names of Branch1 and Branch2. These respective <xref:System.Activities.Statements.PickBranch.DisplayName%2A> property values can be edited in the **PickBranch** activity designer header or within the **Properties** window for each branch.  
  
 There are two ways to add <xref:System.Activities.Statements.PickBranch> activities to the collection of a <xref:System.Activities.Statements.Pick> object: dragging and dropping the **PickBranch** designer from the **Toolbox** or by using the context menu from within the **Pick** design surface. For details, see the [PickBranch](../workflow-designer/pickbranch-activity-designer.md) topic. Notice that the only item that can be placed inside a **Pick** activity designer is a **PickBranch** activity designer.  
  
### Pick Activity Properties in the Workflow Designer  
 The following table shows the <xref:System.Activities.Statements.Pick> properties and describes how they are used in the designer. These properties can be edited in property grid or on the designer surface.  
  
|Property Name|Required|Usage|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName%2A>|False|Specifies the friendly name of the <xref:System.Activities.Statements.Pick> activity designer in the header. The default value is Pick. The value can be edited in the property grid or directly on the header of the activity designer.<br /><br /> Although the <xref:System.Activities.Activity.DisplayName%2A> is not strictly required, it is a best practice to use one.|  
  
## See Also  
 [Control Flow](../workflow-designer/control-flow-activity-designers.md)   
 [Pick Activity](../Topic/Pick%20Activity.md)   
 [Using the Pick Activity](../Topic/Using%20the%20Pick%20Activity.md)