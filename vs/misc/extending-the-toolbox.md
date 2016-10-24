---
title: "Extending the Toolbox | Microsoft Docs"
ms.custom: ""
ms.date: "10/20/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "tools [Visual Studio], Toolbox"
  - "Toolbox [Visual Studio SDK]"
ms.assetid: bb84a79e-cd4c-4a58-8871-2513e7119b6e
caps.latest.revision: 38
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
# Extending the Toolbox
The [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] **Toolbox** provides a collection of objects that provide functionality to editors and designers through the IDE's drag-and-drop mechanism.  
  
 There are two basic ways in which a VSPackage works with the [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] **Toolbox**:  
  
-   A VSPackage can add new data items and controls to the **Toolbox**.  
  
-   A VSPackage can be a target or consumer of existing **Toolbox** functionality, supporting the drag-and-drop operations and configuring the **Toolbox**'s appearance.  
  
## In This Section  
 [How to: Create a Toolbox Control That Uses Windows Forms](../misc/how-to--create-a-toolbox-control-that-uses-windows-forms.md)  
 Describes out to create a Toolbox control by using the Windows Forms Toolbox Control template.  
  
 [Creating a WPF Toolbox Control](../extensibility/creating-a-wpf-toolbox-control.md)  
 Describes out to create a Toolbox control by using the WPF Toolbox Control template.  
  
 [Managing the Toolbox](../misc/managing-the-toolbox.md)  
 Describes how a VSPackage can manage the content and appearance of the **Toolbox**.  
  
## Related Sections  
 [How to: Manage the Toolbox Window](http://msdn.microsoft.com/en-us/a022c3fe-298c-4a59-a48f-b050da90ebc2)  
 Describes how to work with the **Toolbox** in the [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] integrated development environment (IDE).  
  
 [How to: Control the Toolbox](../Topic/How%20to:%20Control%20the%20Toolbox.md)  
 Describes how to manage the **Toolbox** using the automation programming model.  
  
 [Extending Other Parts of Visual Studio](../extensibility/extending-other-parts-of-visual-studio.md)  
 Explains how to use [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] services to create UI elements that match the rest of [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)].