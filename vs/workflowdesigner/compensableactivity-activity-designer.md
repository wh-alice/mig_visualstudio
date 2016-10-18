---
title: "CompensableActivity Activity Designer"
ms.custom: na
ms.date: "10/02/2016"
ms.prod: ".net-framework-4.6"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "reference"
f1_keywords: 
  - "System.Activities.Statements.CompensableActivity.UI"
ms.assetid: e0340d89-d39e-4a52-8557-13e27040d7b5
caps.latest.revision: 6
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
# CompensableActivity Activity Designer
The **CompensableActivity** activity designer is used to create and configure a <xref:System.Activities.Statements.CompensableActivity> activity.  
  
## The CompensableActivity Activity  
 The <xref:System.Activities.Statements.CompensableActivity> defines a unit of work that can be confirmed or compensated after successful completion.  
  
### Using the CompensableActivity Activity Designer  
 The **CompensableActivity** activity designer can be found in the **Transaction** category of the **Toolbox**, which is accessed by clicking the **Toolbox** tab on the left side of the [!INCLUDE[wfd2](../workflowdesigner/includes/wfd2_md.md)] (Alternatively, select **Toolbar** from the **View** menu, or CTRL+ALT+X.)  
  
 The **CompensableActivity** activity designer can be dragged from the **Toolbox** and dropped on to the [!INCLUDE[wfd2](../workflowdesigner/includes/wfd2_md.md)] surface wherever activities are usually placed, such as inside a <xref:System.Activities.Statements.Sequence>. This creates a <xref:System.Activities.Statements.CompensableActivity> activity with a default <xref:System.Activities.Activity.DisplayName*> of CompensableActivity. The <xref:System.Activities.Activity.DisplayName*> value can be edited in the header of the **CompensableActivity** activity designer or in the **DisplayName** box of the property grid.  
  
### The CompensableActivity Properties  
 The following table shows the <xref:System.Activities.Statements.CompensableActivity> properties and describes how they are used in the designer. The <xref:System.Activities.Activity.DisplayName*> and <xref:System.Activities.Activity`1.Result*> property can be edited in property grid but the other properties must be edited on the [!INCLUDE[wfd2](../workflowdesigner/includes/wfd2_md.md)] surface.  
  
|Property Name|Required|Usage|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName*>|False|The optional friendly name of the <xref:System.Activities.Statements.CompensableActivity> activity. The default is CompensableActivity.|  
|<xref:System.Activities.Activity`1.Result*>|False|Specifies the return value of the <xref:System.Activities.Statements.CompensableActivity>. This property must be edited in the property grid.|  
|<xref:System.Activities.Statements.CompensableActivity.Body*>|True|Specifies the activity for which the compensation, cancellation, and confirmation logic is provided. To add the <xref:System.Activities.Statements.CompensableActivity.Body*> activity, drop an activity from the **Toolbox** into the **Body** box on the **CompensableActivity** activity designer with hint text “Drop activity here”.|  
|<xref:System.Activities.Statements.CompensableActivity.CancellationHandler*>|False|Specifies the activity that is executed in the event of cancellation. To add the activity, drop its designer from the **Toolbox** into the **CancellationHandler** box on the **CompensableActivity** activity designer with hint text “Drop Activity Here”.|  
|<xref:System.Activities.Statements.CompensableActivity.CompensationHandler*>|False|Specifies the activity to be executed when compensating for the <xref:System.Activities.Statements.CompensableActivity.Body*> activity. This handler can be explicitly invoked using the <xref:System.Activities.Statements.Compensate> activity.<br /><br /> To add the activity, drop its activity designer from the **Toolbox** into the **CompensationHandler** box on the **CompensableActivity** activity designer with hint text “Drop Activity Here”.|  
|<xref:System.Activities.Statements.CompensableActivity.ConfirmationHandler*>|False|Specifies the activity to be executed when confirming the <xref:System.Activities.Statements.CompensableActivity.Body*> activity. This handler can be explicitly invoked using the <xref:System.Activities.Statements.Confirm> activity.<br /><br /> To add the activity, drop its activity designer from the **Toolbox** into the **ConfirmationHandler** box on the **CompensableActivity** activity designer with hint text “Drop Activity Here”.|  
  
## See Also  
 [Transaction](../workflowdesigner/transaction-activity-designers.md)   
 [CancellationScope](../workflowdesigner/cancellationscope-activity-designer.md)   
 [Compensate](../workflowdesigner/compensate-activity-designer.md)   
 [Confirm](../workflowdesigner/confirm-activity-designer.md)   
 [TransactionScope](../workflowdesigner/transactionscope-activity-designer.md)