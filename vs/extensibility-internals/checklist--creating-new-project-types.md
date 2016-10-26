---
title: "Checklist: Creating New Project Types"
ms.custom: ""
ms.date: "10/21/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "projects [Visual Studio SDK], creating new types"
  - "project types, checklist for creating"
ms.assetid: 29eb9c3b-1933-4741-aa85-65a33f0825ba
caps.latest.revision: 23
ms.author: "gregvanl"
manager: "ghogen"
translation.priority.mt: 
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
# Checklist: Creating New Project Types
You must complete several tasks to create a new project type. The following checklist provides a guide to those tasks.  
  
1.  Design the functionality for your new project type. For more information, see [Project Type Design Decisions](../extensibility-internals/project-type-design-decisions.md).  
  
2.  Determine which editors are used for code and other project elements. You can use the core or standard editors, or you can create and use project-specific editors. For more information, see [Creating Custom Editors and Designers](../extensibility/creating-custom-editors-and-designers.md) and [How to: Open Project-Specific Editors](../extensibility/how-to--open-project-specific-editors.md).  
  
3.  Determine the level of participation your project items will have in the **Class View** and the **Object Browser**. For more information, see [Supporting Symbol-Browsing Tools](../extensibility-internals/supporting-symbol-browsing-tools.md).  
  
4.  Derive new classes based on design decisions that you made previously for your project and project items.  
  
5.  Write the code for the following project type components:  
  
    -   Project factory, to manage creating new projects and opening existing projects. For more information, see [Creating Project Instances By Using Project Factories](../extensibility-internals/creating-project-instances-by-using-project-factories.md).  
  
    -   Project hierarchy and command handling. For more information, see [Not in Build: Using HierUtil7 Project Classes to Implement a Project Type (C++)](http://msdn.microsoft.com/en-us/a5c16a09-94a2-46ef-87b5-35b815e2f346), [Elements of a Project Model](../extensibility-internals/elements-of-a-project-model.md), [Project Model Core Components](../extensibility-internals/project-model-core-components.md) and [MenuCommands Vs. OleMenuCommands](../misc/menucommands-vs.-olemenucommands.md).  
  
    -   Project items management, including adding your project to the **New Project** dialog box. For more information, see [Adding Project and Project Item Templates](../extensibility-internals/adding-project-and-project-item-templates.md) and [Registering Project and Item Templates](../extensibility-internals/registering-project-and-item-templates.md).  
  
    -   Persistence of project state and individual items. For more information, see [Opening and Saving Project Items](../extensibility-internals/opening-and-saving-project-items.md). For persistence of solution information, see [Solutions](../extensibility-internals/solutions.md).  
  
    -   Configuration independent properties to display in the Properties window. For more information, see [Extending Properties](../extensibility-internals/extending-properties.md).  
  
    -   Project configuration properties as implemented in property pages to show configuration-dependent properties. For more information, see [Managing Configuration Options](../extensibility-internals/managing-configuration-options.md).  
  
    -   Enumerating outputs for deployment. For more information, see [Project Configuration for Output](../extensibility-internals/project-configuration-for-output.md).  
  
    -   Project startup services. For more information, see [Elements of a Project Model](../extensibility-internals/elements-of-a-project-model.md) and [Project Model Core Components](../extensibility-internals/project-model-core-components.md).  
  
    -   Objects, or classes derived from `IDispatch`, available for Automation.  
  
    -   XML Command Table (.vsct) files. For more information, see [Visual Studio Command Table (.Vsct) Files](../Topic/Visual%20Studio%20Command%20Table%20\(.Vsct\)%20Files.md).  
  
6.  Test, debug, and start your project type.  
  
7.  Display your project in the **Project** tab of the **Add Reference** dialog box by setting `VARIANT_TRUE` as the value for `VSHPROPID_ShowProjInSolutionPage`. For more information, see <xref:Microsoft.VisualStudio.Shell.Interop.__VSHPROPID> and <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy.GetProperty*>.  
  
8.  Create the Microsoft Installer (.msi) file for installing your VSPackages. For more information, see [Installing VSPackages With Windows Installer](../extensibility-internals/installing-vspackages-with-windows-installer.md), [Registering a Project Type](../extensibility-internals/registering-a-project-type.md), and [VSPackages](../extensibility-internals/vspackages.md).  
  
## See Also  
 [Hierarchies in Visual Studio](../extensibility-internals/hierarchies-in-visual-studio.md)   
 [When to Create Project Types](../extensibility-internals/when-to-create-project-types.md)   
 [Creating Project Types](../extensibility-internals/creating-project-types.md)