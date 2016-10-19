---
title: "Supporting Source Control"
ms.custom: ""
ms.date: "10/18/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "source control [Visual Studio SDK], supporting"
ms.assetid: 567acde3-354e-4f39-8d99-0ef86c103396
caps.latest.revision: 18
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
# Supporting Source Control
[!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] supports file checkouts, check-ins, and other source control operations for your project or editor. As a source control client, [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] is designed to interact with a source control package, such as [!INCLUDE[vsvss](../extensibility/includes/vsvss_md.md)], which provides archiving, versioning, and control facilities for a dynamically defined set of files.  
  
## In This Section  
 [Model for Source Control Packages](../extensibility/model-for-source-control-packages.md)  
 Describes the interfaces a project type must implement to support source control.  
  
 [Design Decisions](../extensibility/source-control-design-decisions.md)  
 Provides questions whose answers change how you implement a project type.  
  
 [Configuration Details](../extensibility/source-control-configuration-details.md)  
 Describes how supporting source control changes the implementation of a project type.  
  
 [Additional Guidelines for Projects and Editors](../extensibility/additional-source-control-guidelines-for-projects-and-editors.md)  
 Discusses best practices for project types and editors.  
  
 [Runtime Details](../extensibility/source-control-runtime-details.md)  
 Describes how to register a project when a user adds it to a source-control system.  
  
## Reference  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsQueryEditQuerySave2>  
 Indicates to the environment or source control package that a file is about to be changed in memory or saved.  
  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsSccManager2>  
 Allows projects and hierarchies to register themselves with source control and obtain information about source control status.  
  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsSccProject2>  
 Implemented in a project system to provide source control for project files and project items.  
  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsTrackProjectDocuments2>  
 Used by projects to query the environment for permission to add, remove, or rename a file or directory in a solution.  
  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsTrackProjectDocumentsEvents2>  
 Notifies clients of changes that were made to project files or directories.  
  
## Related Sections  
 [Project Types](../extensibility/project-types.md)  
 Provides an overview of projects as the basic building blocks of the [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] integrated development environment (IDE). Links are provided to additional topics that explain how projects control building and compiling code.