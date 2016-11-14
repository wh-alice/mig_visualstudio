---
title: "How to: Use the Argument Designer | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.prod: ".net-framework-4.6"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "System.Activities.Presentation.View.ArgumentDesigner.UI"
  - "System.Activities.Presentation.View.DesignTimeArgument.UI"
ms.assetid: 64813fd5-1ea1-499a-98b4-ab2a44b7ee5e
caps.latest.revision: 16
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
# How to: Use the Argument Designer
Compared to previous versions of the [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)], the argument designer makes it easy to allow data to flow into and out of an activity. The designer is accessed by clicking the **Arguments** button in the lower-left corner of the design canvas. The designer contains a list of arguments that appear in a tabular form and can be sorted by each of the column headers, except for the **Default value** column. Each argument contains a name, in/out/in-out/property direction, type, and default expression value (if any). The name and the default expression value are editable text fields, and the type and direction are drop-downs. [!INCLUDE[crabout](../test/includes/crabout_md.md)] arguments, see [Variables and Arguments](http://msdn.microsoft.com/en-us/Library/d03dbe34-5b2e-4f21-8b57-693ee49611b8).  
  
### To create a new argument  
  
1.  Open a workflow or activity solution in [!INCLUDE[vs2010](../misc/includes/vs2010_md.md)].  
  
2.  Open the arguments designer by clicking the **Arguments** button in the lower-left corner of the design canvas. The arguments designer appears.  
  
3.  Click the empty row labeled **Create Argument**. This will add a new row with a new argument using the following default values: argumentx for the **Name** where x is an integer with an initial value of 1 that is automatically incremented to create unique argument names, **In** for the **Direction**, and **String** for the **Argument type**. No value is added for **Default value**. You can change these values at any time during the workflow design process.  
  
    > [!NOTE]
    >  To delete an argument, select the argument by clicking it and then press the **Delete** key.  
  
## See Also  
 [Using the Workflow Designer](../workflow-designer/using-the-workflow-designer.md)   
 [Variables and Arguments](http://msdn.microsoft.com/en-us/Library/d03dbe34-5b2e-4f21-8b57-693ee49611b8)