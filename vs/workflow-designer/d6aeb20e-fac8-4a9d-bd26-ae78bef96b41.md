---
title: "How to: Implement a Windows Communication Foundation Contract Operation (Legacy)"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: ".net-framework-4.6"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "reference"
ms.assetid: d6aeb20e-fac8-4a9d-bd26-ae78bef96b41
caps.latest.revision: 7
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
# How to: Implement a Windows Communication Foundation Contract Operation (Legacy)
This topic describes how to implement a [!INCLUDE[indigo1](../workflow-designer/includes/indigo1_md.md)] contract operation using the legacy [!INCLUDE[wfd1](../workflow-designer/includes/wfd1_md.md)] that targets the [!INCLUDE[netfx35_long](../workflow-designer/includes/netfx35_long_md.md)] or the [!INCLUDE[vstecwinfx](../workflow-designer/includes/vstecwinfx_md.md)].  
  
 After dragging a **ReceiveActivity** activity from the toolbox to the workflow design surface, you will either create a new [!INCLUDE[indigo2](../workflow-designer/includes/indigo2_md.md)] contract or import an existing contract and implement the operations. You select and/or create your contract and its operations through the [Choose Operation Dialog Box (Legacy)](../workflow-designer/choose-operation-dialog-box--legacy-.md).  
  
### To implement a WCF contract operation  
  
1.  Double-click the **ReceiveActivity** activity in the designer or click the ellipsis next to the **ServiceOperationInfo** property in the **Properties** pane.  
  
2.  Do one of the following:  
  
    -   Click **Add Contract** in the upper-right corner of the dialog box. This will create a new [!INCLUDE[indigo2](../workflow-designer/includes/indigo2_md.md)] contract and operation for you.  
  
         -or-  
  
    -   Click **Import** in the upper-right corner of the dialog box. The [Browse and Select a .NET Type Dialog Box (Legacy)](../workflow-designer/browse-and-select-a-.net-type-dialog-box--legacy-.md) opens. Search for an assembly or project that contains the contract you want. Select the contract and click **OK**.  
  
     After a contract is created or imported, you can add new operations to that created or imported contract. To add a new operation, select the contract and click **Add Operation** in the upper-right corner of the dialog box. When you are done adding operations, proceed to step 3.  
  
3.  Select the operation you want to associate with the **ReceiveActivity** activity. You can manipulate the definition of the operation by changing the operation's name, parameters, properties, and permission settings.  
  
     To change the name, enter the new name in the **Operation Name** text box.  
  
     Click the **Parameters** tab to access the operation's parameters. You can change the name, type, or direction of a parameter as well as add or delete parameters from the operation.  
  
     Click the **Properties** tab to access the operation protection level and supported message exchange functionality of the operation.  
  
     Click the **Permissions** tab to specify which group(s) are allowed to implement the operation.  
  
4.  Click **OK** and the **ReceiveActivity** activity will display the operation name for the operation that it is implementing.  
  
5.  Place the workflow activities you are going to use for the implementation of that operation within the **ReceiveActivity** activity.  
  
## See Also  
 [Choose Operation Dialog Box (Legacy)](../workflow-designer/choose-operation-dialog-box--legacy-.md)   
 [How to: Invoke a WCF Contract Operation (Legacy)](../workflow-designer/how-to--invoke-a-windows-communication-foundation-contract-operation--legacy-.md)   
 [Legacy Workflow Activities](../workflow-designer/legacy-workflow-activities.md)