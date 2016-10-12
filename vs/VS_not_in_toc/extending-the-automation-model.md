---
title: "Extending the Automation Model"
ms.custom: na
ms.date: "10/01/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "automation object model, extending"
ms.assetid: f09e1365-6291-41a7-b52b-9398270d9da2
caps.latest.revision: 12
manager: "douge"
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
# Extending the Automation Model
This section discusses how the automation model and the VSPackage model represent a two-prong approach to extensibility in the [!INCLUDE[vsprvs](../dv_TeamTestALM/includes/vsprvs_md.md)] environment. Extensibility is the capacity to enhance and extend the functionality of the IDE. Automation, on the one hand, refers to user-created code and tools that automate tasks in the existing environment and programmatically drive the IDE. VSPackages, on the other hand, let you add new functionality to the environment.  
  
 It is possible to combine automation and VSPackages in an extensibility application. For an example, see [Walkthrough: Extending Managed VSPackages By Using Automation](../VS_not_in_toc/walkthrough--extending-managed-vspackages-by-using-automation.md).  
  
 For an end-to-end sample of a language project system that supports the automation model, see the [VSSDK Samples](../VS_not_in_toc/vssdk-samples.md).  
  
## In This Section  
 [Automation Model](../VS_not_in_toc/automation-model.md)  
 Provides an overview of the automation model and discusses how the automation model lets you customize, adjust, and automate the environment.  
  
 [Contributing to the Automation Model](../Topic/Contributing%20to%20the%20Automation%20Model.md)  
 Provides a more detailed view of the automation model and discusses the ways to provide automation for your VSPackage. This section also provides code examples that show how an automation consumer obtains the initial project automation objects.  
  
## Related Sections  
 [Visual Studio SDK and Automation](../Topic/Visual%20Studio%20SDK%20and%20Automation.md)  
 Discusses using automation, VSPackages, or a combination to create [!INCLUDE[vsprvs](../dv_TeamTestALM/includes/vsprvs_md.md)] extensibility applications.