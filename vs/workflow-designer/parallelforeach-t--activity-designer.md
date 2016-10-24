---
title: "ParallelForEach&lt;T&gt; Activity Designer | testtitle"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: ".net-framework-4.6"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "System.Activities.Statements.ParallelForEach`1.UI"
ms.assetid: e93a4843-aef2-4d3e-9a0a-a2d3d1411aa7
caps.latest.revision: 9
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
# ParallelForEach&lt;T&gt; Activity Designer
The <xref:System.Activities.Statements.ParallelForEach`1> activity enumerates the elements of a collection and executes an embedded statement for each element of the collection in parallel, which is asynchronously on the same thread. Use this flow control activity instead of the <xref:System.Activities.Statements.Sequence> activity if the child activities of this activity are expected to go idle.  
  
 The <xref:System.Activities.Statements.ParallelForEach`1> activity has a <xref:System.Activities.Statements.ParallelForEach`1.CompletionCondition*> property that contains a user specified [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] expression. The <xref:System.Activities.Statements.ParallelForEach`1> activity evaluates this property after each branch completes. If it evaluates to **true**, then the <xref:System.Activities.Statements.ParallelForEach`1> activity completes without executing the other branches. If the <xref:System.Activities.Statements.ParallelForEach`1.CompletionCondition*> does not evaluate to **true**, then the <xref:System.Activities.Statements.ParallelForEach`1> activity completes when all of its child activities have completed.  
  
## The ParallelForEach<T\> Activity  
 <xref:System.Activities.Statements.ParallelForEach`1> enumerates its values and schedules the <xref:System.Activities.Statements.ParallelForEach`1.Body*> for every value it enumerates on. It only schedules the <xref:System.Activities.Statements.ParallelForEach`1.Body*>. How the body executes depends on whether the <xref:System.Activities.Statements.ParallelForEach`1.Body*> goes idle.  
  
 If the <xref:System.Activities.Statements.ParallelForEach`1.Body*> does not go idle, it executes in a reverse order because the scheduled activities are handled as a stack, the last scheduled activity executes first. For example, if you have a collection of {1,2,3,4}in <xref:System.Activities.Statements.ParallelForEach`1> and use a **WriteLine** as the body to write the value out. You have 4, 3, 2, 1 printed out in the console. This is because **WriteLine** does not go idle so after 4 **WriteLine** activities got scheduled, they executed using a stack behavior (first in last out).  
  
 But if you have activities in the <xref:System.Activities.Statements.ParallelForEach`1.Body*> that can go idle, like a <xref:System.ServiceModel.Activities.Receive> activity or <xref:System.Activities.Statements.Delay> activity. Then there is no need to wait for them to complete. <xref:System.Activities.Statements.ParallelForEach`1> goes to the next scheduled body activity and try to execute it. If that activity goes idle too, <xref:System.Activities.Statements.ParallelForEach`1> moves on again the next body activity.  
  
### Using the ParallelForEach\<T> Activity Designer  
 The **ParallelForEach\<T>** activity designer can be found in the **Control Flow** category of the **Toolbox**, which is accessed by clicking the **Toolbox** tab on the left side of the [!INCLUDE[wfd2](../workflow-designer/includes/wfd2_md.md)] (Alternatively, select **Toolbar** from the **View** menu, or CTRL+ALT+X.)  
  
 The **ParallelForEach\<T>** activity designer can be dragged from the **Toolbox** and dropped on to the [!INCLUDE[wfd2](../workflow-designer/includes/wfd2_md.md)] surface wherever activity designers are normally placed, for example, inside of a **Sequence** activity designer. After dropping it into the [!INCLUDE[wfd2](../workflow-designer/includes/wfd2_md.md)], it creates a <xref:System.Activities.Statements.ParallelForEach`1> activity, which by default contains a <xref:System.Activities.Activity.DisplayName*> of **ParallelForEach<Int32\>.**  
  
### ParallelForEach<T\> Properties in the Workflow Designer  
 The following table shows the most useful <xref:System.Activities.Statements.ParallelForEach`1> activity properties and describes how they are used in the designer.  
  
|Property Name|Required|Usage|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName*>|False|Specifies the friendly display name of the activity designer in the header. The default value is **ParallelForEach\<Int32>**. The value can be optionally edited in the **Properties** grid or directly on the activity designer header.|  
|<xref:System.Activities.Statements.ParallelForEach`1.Body*>|False|The activity to execute for each item in the collection. To add the <xref:System.Activities.Statements.ParallelForEach`1.Body*> activity, drop an activity from the toolbox into the **Body** box on the **ParallelForEach\<T>** activity designer with hint text “Drop Activity Here”.|  
|**TypeArgument**|True|The type of the items in the <xref:System.Activities.Statements.ParallelForEach`1.Values*> collection specified by the generic parameter *T*. By default, **TypeArgument** is set to **Int32**. To change the type T in the **ParallelForEach<T\>** activity designer, change the value of the **TypeArgument** combo box in the Property Grid.|  
|<xref:System.Activities.Statements.ParallelForEach`1.Values*>|True|The collection of items to iterate over. To set the <xref:System.Activities.Statements.ParallelForEach`1.Values*>, type a [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] expression in the **Values** box on the **ForEach<T\>** activity designer in the box with the hint text “Enter a VB expression” or in **Values** box on the **Properties** window.|  
|<xref:System.Activities.Statements.ParallelForEach`1.CompletionCondition*>||Evaluated after each iteration completes. If it evaluates to true, then the scheduled pending iterations are canceled. If this property is not set, all scheduled statements execute until completion.|  
  
 By default, the loop iterator is named item. You can change the name of the iterator variable in the **ForEach** box in **ParallelForEach\<T>** activity designer. The loop iterator can be used in expressions in the children of the <xref:System.Activities.Statements.ParallelForEach`1> activity.  
  
## See Also  
 [Sequence](../workflow-designer/sequence-activity-designer.md)   
 [Parallel](../workflow-designer/parallel-activity-designer.md)   
 [Control Flow](../workflow-designer/control-flow-activity-designers.md)