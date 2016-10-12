---
title: "FinalState Activity Designer"
ms.custom: na
ms.date: "10/02/2016"
ms.prod: ".net-framework-4.6"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "reference"
ms.assetid: aa186893-8775-40dd-981f-8593ead831d0
caps.latest.revision: 5
ms.author: "sdanie"
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
# FinalState Activity Designer
The \<xref:System.Activities.Core.Presentation.FinalState> designer is used to create a \<xref:System.Activities.Statements.State> that terminates a state machine instance.  
  
## Using the FinalState Activity Designer  
 The **FinalState** designer is used to create a \<xref:System.Activities.Statements.State> that is preconfigured as a terminating state in a state machine. A \<xref:System.Activities.Statements.State> that is created using the \<xref:System.Activities.Core.Presentation.FinalState> activity designer has its \<xref:System.Activities.Statements.State.IsFinal*> property set to **true**, has no \<xref:System.Activities.Statements.State.Exit*> activity and no transitions originating from it. To use the \<xref:System.Activities.Core.Presentation.FinalState> activity designer to add a \<xref:System.Activities.Statements.State> activity that is preconfigured as a terminating state in a state machine, drag the **FinalState** activity designer from the **State Machine** section of the **Toolbox** and drop it onto the workflow designer. The \<xref:System.Activities.Core.Presentation.FinalState> activity designer can be dropped onto a \<xref:System.Activities.Statements.StateMachine> and transitions added later; or a transition can be created as the \<xref:System.Activities.Core.Presentation.FinalState> activity designer is dropped. For more information on creating transitions, see [Transition](../WF_Design/transition-activity-designer.md).  
  
### State Activity Properties in the Workflow Designer  
 The following table shows the properties that can be set using the \<xref:System.Activities.Core.Presentation.FinalState> designer and describes how they are used in the designer. Some of these properties can be edited in the property grid and some can be edited on the designer surface.  
  
|Property Name|Required|Usage|  
|-------------------|--------------|-----------|  
|\<xref:System.Activities.Statements.State.DisplayName*>|False|Specifies the friendly name of the \<xref:System.Activities.Statements.State> activity designer in the header. The default value is **State**. The value can be edited in the property grid or directly on the header of the activity designer. The \<xref:System.Activities.Statements.State.DisplayName*> is used in the breadcrumb navigation that is displayed at the top of the workflow designer.<br /><br /> Although the \<xref:System.Activities.Statements.State.DisplayName*> is not strictly required, it is a best practice to use one.|  
|\<xref:System.Activities.Statements.State.Entry*>|False|Specifies the action that occurs when this state is transitioned to. This value can be set by dragging an activity from the **Toolbox** and dropping it onto the \<xref:System.Activities.Statements.State.Entry*> section of the state.|  
  
## See Also  
 [StateMachine](../WF_Design/statemachine-activity-designer.md)   
 [State](../WF_Design/state-activity-designer.md)   
 [Transition](../WF_Design/transition-activity-designer.md)