---
title: "Send Activity Designer"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: ".net-framework-4.6"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "System.ServiceModel.Activities.Send.UI"
ms.assetid: b514f2e4-767c-4b94-ac61-dd3a54d4b96d
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
# Send Activity Designer
The **Send** activity designer is used to create and configure a <xref:System.ServiceModel.Activities.Send> activity.  
  
## The Send Activity  
 A <xref:System.ServiceModel.Activities.Send> activity is used to send a message to a service. A <xref:System.ServiceModel.Activities.ReceiveReply> activity can be bound to a <xref:System.ServiceModel.Activities.Send> activity that receives a message as part of a request/response message exchange pattern on the client.  
  
### Using the Send Activity Designer  
 The **Send** activity designer can be found in the **Messaging** category of the **Toolbox**, which is accessed by clicking the **Toolbox** tab in [!INCLUDE[wfd2](../workflow-designer/includes/wfd2_md.md)] (Alternatively, select **Toolbar** from the **View** menu or CTRL+ALT+X.)  
  
 The **Send** activity designer can be dragged from the **Toolbox** and dropped on to the [!INCLUDE[wfd2](../workflow-designer/includes/wfd2_md.md)] surface wherever activities are usually placed. This creates a <xref:System.ServiceModel.Activities.Send> activity with a default <xref:System.Activities.Activity.DisplayName*> of Send. The <xref:System.Activities.Activity.DisplayName*> can be edited in the header of the **Send** activity designer or in the **DisplayName** box of the property grid.  
  
 To create a <xref:System.ServiceModel.Activities.ReceiveReply> activity and bind it to the selected <xref:System.ServiceModel.Activities.Send> activity, right-click the **Send** activity designer, click the **Create ReceiveReply** item in the context menu and the **ReceiveReplyForSend** designer appears below the **Send** designer. The <xref:System.ServiceModel.Activities.ReceiveReply> activity is an activity that receives a message as part of a request/response message exchange pattern on the client. It can be configured with the **ReceiveReplyForSend** designer.  
  
 Alternatively, the **SendAndReceiveReply** template designer in the **Messaging** category of the **Toolbox** can be used to create a pair of pre-configured <xref:System.ServiceModel.Activities.Send> and <xref:System.ServiceModel.Activities.ReceiveReply> activities. [!INCLUDE[crabout](../test/includes/crabout_md.md)] the use of the **SendAndReceiveReply** and **ReceiveReplyForSend** templates, see the [SendAndReceiveReply](../workflow-designer/sendandreceivereply-template-designer.md) topic.  
  
### The Send Activity Properties  
 The following table shows the <xref:System.ServiceModel.Activities.Send> properties and describes how they are used in the designer. These properties can be edited in properties grid or on [!INCLUDE[wfd2](../workflow-designer/includes/wfd2_md.md)] surface.  
  
|Property Name|Required|Usage|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName*>|False|The friendly name of the <xref:System.ServiceModel.Activities.Send> activity. The default is Send. Although the <xref:System.Activities.Activity.DisplayName*> is not strictly required, it is a best practice to use one.|  
|<xref:System.ServiceModel.Activities.Send.OperationName*>|True|The name of the service operation called by this <xref:System.ServiceModel.Activities.Send> activity. This property is used to construct the default value for the **Action** property if the **Action** property is not explicitly set.|  
|<xref:System.ServiceModel.Activities.Send.ServiceContractName*>|True|The name of the service contract that the service to be called implements.|  
|<xref:System.ServiceModel.Activities.Send.Content*>|False|Specifies the message or parameter content to receive. It can be either a <xref:System.ServiceModel.Activities.ReceiveMessageContent> activity or a <xref:System.ServiceModel.Activities.ReceiveParametersContent> activity. Edit this property by clicking the ellipse button beside the **Content** field in property grid or clicking the **Define…** button beside the **Content** label on the **Receive** activity designer surface. Both display the **Content Definition** dialog. [!INCLUDE[crabout](../test/includes/crabout_md.md)] how to use this box, see the [Content Definition Dialog Box](../workflow-designer/content-definition-dialog-box.md) topic.|  
|<xref:System.ServiceModel.Activities.Send.CorrelatesWith*>|False|Specifies the <xref:System.ServiceModel.Activities.CorrelationHandle> used to route the message to the appropriate workflow instance.<br /><br /> Click the ellipsis button next to the <xref:System.ServiceModel.Activities.Send.CorrelatesWith*> property in the properties grid to open the **Expression Editor** dialog box. [!INCLUDE[crabout](../test/includes/crabout_md.md)] the use of this dialog box, see the [How to: Use the Expression Editor](../workflow-designer/how-to--use-the-expression-editor.md) topic.|  
|<xref:System.ServiceModel.Activities.Send.CorrelationInitializers*>|False|Specifies the collection of <xref:System.ServiceModel.Activities.CorrelationInitializer> objects that initialize multiple <xref:System.ServiceModel.Activities.CorrelationHandle> objects that configure this <xref:System.ServiceModel.Activities.Send> activity within the workflow. Click the ellipsis button next to the <xref:System.ServiceModel.Activities.Send.CorrelationInitializers*> property in the properties grid to open the **Add Correlation Initializers** dialog box. [!INCLUDE[crabout](../test/includes/crabout_md.md)] using this box, see the [Add CorrelationInitializers Dialog Box](../workflow-designer/add-correlationinitializers-dialog-box.md) topic.|  
|<xref:System.ServiceModel.Activities.Send.KnownTypes*>|False|A collection of known types for the service operation to be called by this <xref:System.ServiceModel.Activities.Send> activity. This property should be used in conjunction with <xref:System.ServiceModel.Activities.Receive.SerializerOption*> property set to <xref:System.Runtime.Serialization.DataContractSerializer>. It is ignored if <xref:System.Xml.Serialization.XmlSerializer> is used.<br /><br /> Click the ellipse button beside the **KnownTypes** field in property grid to display the **Type Collection Editor** dialog with which you can add relevant types.<br /><br /> Click the ellipse button beside the **KnownTypes** field in property grid to display the **Type Collection Editor** dialog box with which you can add relevant types. [!INCLUDE[crabout](../test/includes/crabout_md.md)] using this box, see the [Type Collection Editor Dialog Box](../workflow-designer/type-collection-editor-dialog-box.md) topic.|  
|<xref:System.ServiceModel.Activities.Send.ProtectionLevel*>|True|Specifies the <xref:System.Net.Security.ProtectionLevel> for the message.<br /><br /> 1.  <xref:System.Net.Security.ProtectionLevel> means authentication only.<br />2.  <xref:System.Net.Security.ProtectionLevel> means sign data to help ensure the integrity of transmitted data.<br />3.  <xref:System.Net.Security.ProtectionLevel> means encrypt and sign data to help ensure the confidentiality and integrity of transmitted data.|  
|<xref:System.ServiceModel.Activities.Send.SerializerOption*>|True|The serializer to use for the service operation to be called by the <xref:System.ServiceModel.Activities.Send> activity. The default value is <xref:System.Runtime.Serialization.DataContractSerializer>, which serializes and deserializes an instance of a type into an XML stream or document using a supplied data contract.|  
|<xref:System.ServiceModel.Activities.Send.Action*>|False|Specifies the action header of the message. If it is not explicitly set, its value defaults to: https://tempuri.org/{service contract namespace}/{service contract name}/{operation name}. If specified on a <xref:System.ServiceModel.Activities.Send> activity, the <xref:System.ServiceModel.Activities.Receive> activity that receives the message must have the same value for the message to be delivered correctly.|  
|<xref:System.ServiceModel.Activities.Send.TokenImpersonationLevel*>||The <xref:System.Security.Principal.TokenImpersonationLevel> allowed for the receiver of the message. It defines security impersonation levels which govern the degree to which a server process can act on behalf of a client process.<xref:System.Security.Principal.TokenImpersonationLevel> indicates that an impersonation level is not assigned. <xref:System.Security.Principal.TokenImpersonationLevel> indicates that the server process cannot obtain identification information about the client and it cannot impersonate the client. <xref:System.Security.Principal.TokenImpersonationLevel> indicates that the server process can obtain information about the client, such as security identifiers and privileges, but that it cannot impersonate the client. This is useful for servers that export their own objects, for example, database products that export tables and views. Using the retrieved client-security information, the server can make access-validation decisions without being able to use other services that are using the client's security context. <xref:System.Security.Principal.TokenImpersonationLevel> indicates that the server process can impersonate the client's security context on its local system. The server cannot impersonate the client on remote systems. <xref:System.Security.Principal.TokenImpersonationLevel> indicates that the server process can impersonate the client's security context on remote systems.|  
|<xref:System.ServiceModel.Activities.Send.Endpoint*>||The <xref:System.ServiceModel.Endpoint> that the <xref:System.ServiceModel.Activities.Send> activity sends the message to. If this property is set the <xref:System.ServiceModel.Activities.Send.EndpointConfigurationName*> property should be **null**.|  
|<xref:System.ServiceModel.Activities.Send.EndpointAddress*>||The <xref:System.ServiceModel.EndpointAddress> to which the message is sent.|  
|<xref:System.ServiceModel.Activities.Send.EndpointConfigurationName*>||The name of the endpoint configuration. This property is set when you are configuring an endpoint in a configuration file. This property should be set to the name given in the **\<endpoint>** element in your configuration file. If this property is set, the <xref:System.ServiceModel.Activities.Send.Endpoint*> property should be **null**.|  
  
## See Also  
 [InitializeCorrelation](../workflow-designer/initializecorrelation-activity-designer.md)   
 [CorrelationScope](../workflow-designer/correlationscope-activity-designer.md)   
 [ReceiveAndSendReply](../workflow-designer/receiveandsendreply-template-designer.md)   
 [Receive](../workflow-designer/receive-activity-designer.md)   
 [SendAndReceiveReply](../workflow-designer/sendandreceivereply-template-designer.md)   
 [TransactedReceiveScope](../workflow-designer/transactedreceivescope-activity-designer.md)