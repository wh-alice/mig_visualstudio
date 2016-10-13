---
title: "Command Availability"
ms.custom: na
ms.date: "10/10/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "commands, context"
  - "menu items, visibility contexts"
ms.assetid: c74e3ccf-d771-48c8-a2f9-df323b166784
caps.latest.revision: 34
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
# Command Availability
The Visual Studio context determines which commands are available. The context can change depending on the current project, the current editor, the VSPackages that are loaded, and other aspects of the integrated development environment (IDE).  
  
## Command Contexts  
 The following command contexts are the most common.  
  
-   **IDE** Commands provided by the IDE are always available.  
  
-   **VSPackage** VSPackages can define when commands are to be displayed or hidden.  
  
-   **Project** Project commands appear only for the currently selected project.  
  
-   **Editor** Only one editor can be active at a time. Commands from the active editor are available. An editor works closely with a language service. The language service must process its commands in the context of the associated editor.  
  
-   **File type** An editor can load more than one type of file. The available commands can change depending on the file type.  
  
-   **Active window** The last active document window sets the user interface (UI) context for key bindings. However, a tool window that has a key-binding table that resembles the internal Web browser could also set the UI context. For multi-tabbed document windows such as the HTML editor, every tab has a different command context GUID. After a tool window is registered, it is always available on the **View** menu.  
  
-   **UI Context** UI contexts are identified by the values of the \<xref:Microsoft.VisualStudio.VSConstants.UICONTEXT> class, for example, \<xref:Microsoft.VisualStudio.VSConstants.UICONTEXT_SolutionBuilding> when the solution is being built, or \<xref:Microsoft.VisualStudio.VSConstants.UICONTEXT_Debugging> when the debugger is active. Multiple UI contexts can be active at the same time.  
  
## Defining Custom Context GUIDs  
 If an appropriate command context GUID is not already defined, you can define one in your VSPackage and then program it to be active or inactive as required to control the visibility of your commands.  
  
1.  Register context GUIDs by calling the \<xref:Microsoft.VisualStudio.Shell.Interop.IVsMonitorSelection.GetCmdUIContextCookie*> method.  
  
2.  Get the state of a context GUID by calling the \<xref:Microsoft.VisualStudio.Shell.Interop.IVsMonitorSelection.IsCmdUIContextActive*> method.  
  
3.  Turn context GUIDs on and off by calling the \<xref:Microsoft.VisualStudio.Shell.Interop.IVsMonitorSelection.SetCmdUIContext*> method.  
  
    > [!CAUTION]
    >  Make sure that your VSPackage does not affect any existing context GUIDs because other VSPackages may depend on them.  
  
## See Also  
 [Selection Context Objects](../extensibility/selection-context-objects.md)   
 [How VSPackages Add User Interface Elements](../extensibility/how-vspackages-add-user-interface-elements.md)