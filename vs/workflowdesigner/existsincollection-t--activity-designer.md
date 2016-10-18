---
title: "ExistsInCollection&lt;T&gt; Activity Designer"
ms.custom: na
ms.date: "10/02/2016"
ms.prod: ".net-framework-4.6"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "reference"
f1_keywords: 
  - "System.Activities.Statements.ExistsInCollection`1.UI"
ms.assetid: 0acf9a13-caf5-4bb4-ba22-ec37d2b7267a
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
# ExistsInCollection&lt;T&gt; Activity Designer
The **ExistsInCollection\<T>** activity designer is used to create and configure an <xref:System.Activities.Statements.ExistsInCollection`1> activity.  
  
## The ExistsInCollection<T\> Activity  
 The <xref:System.Activities.Statements.ExistsInCollection`1> activity determines whether a specified item exists in a particular collection.  
  
### Using the ExistsInCollection\<T> Activity Designer  
 The **ExistsInCollection\<T>** activity designer can be found in the **Collection** category of the **Toolbox**, which is accessed by clicking the **Toolbox** tab of [!INCLUDE[wfd2](../workflowdesigner/includes/wfd2_md.md)] (Alternatively, select **Toolbar** from the **View** menu or CTRL+ALT+X.)  
  
 The **ExistsInCollection\<T>** activity designer can be dragged from the **Toolbox** and dropped on to the [!INCLUDE[wfd2](../workflowdesigner/includes/wfd2_md.md)] surface wherever activities are usually placed, such as inside a <xref:System.Activities.Statements.Sequence>. This creates a <xref:System.Activities.Statements.ExistsInCollection`1> activity with a default <xref:System.Activities.Activity.DisplayName*> of ExistsInCollection<Int32\>. (By default, the *TypeArgument* is **Int32**. It can be changed in the property grid.)  The <xref:System.Activities.Activity.DisplayName*> value can be edited in the header of the **ExistsInCollection<T\>** activity designer or in the **DisplayName** box of the property grid. The other properties must be edited on the property grid.  
  
### The ExistsInCollection<T\> Properties  
 The following table shows the <xref:System.Activities.Statements.ExistsInCollection`1> properties and describes how they are used in the designer.  
  
|Property Name|Required|Usage|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName*>|False|The friendly name of the <xref:System.Activities.Statements.ExistsInCollection`1> activity. The default is ExistsInCollection<Int32\>. Although the <xref:System.Activities.Activity.DisplayName*> value is not strictly required, it is a best practice to use one.|  
|<xref:System.Activities.Statements.ExistsInCollection`1.Item*>|True|The item to add to the Collection\<T>. This item is of type *T* is of type *TypeArgument*. To specify the item, type a Visual Basic expression in the property grid.|  
|<xref:System.Activities.Statements.ExistsInCollection`1.Collection*>|True|The collection to which the item should be added. This collection is of type **ICollection<TypeArgument\>.** To specify the collection, type a Visual Basic expression in the property grid.|  
|*TypeArgument*|True|The type T of the items contained in the <xref:System.Collections.Generic.ICollection`1>. By default, this *TypeArgument* type is set to **Int32**. To change the type, change the value of the *TypeArgument* in the combo box in the property grid.|  
|<xref:System.Activities.Activity`1.Result*>|False|A value that indicates whether the specified item exists in the collection. To specify a variable to bind to the result, type a Visual Basic variable in the property grid.|  
  
## See Also  
 [Collection](../workflowdesigner/collection-activity-designers.md)   
 [AddToCollection\<T>](../workflowdesigner/addtocollection-t--activity-designer.md)   
 [ClearCollection\<T>](../workflowdesigner/clearcollection-t--activity-designer.md)   
 [RemoveFromCollection\<T>](../workflowdesigner/removefromcollection-t--activity-designer.md)