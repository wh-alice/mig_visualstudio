---
title: "Implementing Command Handling for Nested Projects | Microsoft Docs"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "nested projects, implementing command handling"
ms.assetid: 48a9d66e-d51c-4376-a95a-15796643a9f2
caps.latest.revision: 13
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
# Implementing Command Handling for Nested Projects
The IDE can pass commands that are passed through the <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy> and the <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget> interfaces to nested projects, or parent projects can filter or override the commands.  
  
> [!NOTE]
>  Only commands ordinarily handled by the parent project can be filtered. Commands such as **Build** and **Deploy** that are handled by the IDE cannot be filtered.  
  
 The following steps describe the process for implementing command handling.  
  
## Procedures  
  
#### To implement command handling  
  
1.  When the user selects a nested project or a node in a nested project:  
  
    1.  The IDE calls the <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget.QueryStatus*> method.  
  
     — or —  
  
    1.  If the command originated in a hierarchy window, such as a shortcut menu command in Solution Explorer, the IDE calls the <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy.QueryStatusCommand*> method on the project's parent.  
  
2.  The parent project can examine parameters to be passed to `QueryStatus`, such as `pguidCmdGroup` and `prgCmds`, to determine whether the parent project should filter the commands. If the parent project is implemented to filter commands, it should set:  
  
    ```  
    prgCmds[0].cmdf = OLECMDF_SUPPORTED;  
    // make sure it is disabled  
    prgCmds[0].cmdf &= ~MSOCMDF_ENABLED;  
    ```  
  
     Then the parent project should return `S_OK`.  
  
     If the parent project does not filter the command, it should just return `S_OK`. In this case, the IDE automatically routes the command to the child project.  
  
     The parent project does not have to route the command to the child project. The IDE performs this task..  
  
## See Also  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy>   
 [Commands, Menus, and Toolbars](../Topic/Commands,%20Menus,%20and%20Toolbars.md)   
 [Nesting Projects](../extensibility-internals/nesting-projects.md)