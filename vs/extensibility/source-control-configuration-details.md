---
title: "Source Control Configuration Details"
ms.custom: ""
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "source control [Visual Studio SDK], configuration details"
ms.assetid: adbee9fc-7a2e-4abe-a3b8-e6615bcd797f
caps.latest.revision: 11
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
# Source Control Configuration Details
In order to implement source control, you need to properly configure your project system or editor to do the following:  
  
-   Request permission to transition to changed state  
  
-   Request permission to save a file  
  
-   Request permission to add, remove, or rename files in the project  
  
## Request Permission to Transition to Changed State  
 A project or editor must request permission to transition to the changed (dirty) state by calling <xref:Microsoft.VisualStudio.Shell.Interop.IVsQueryEditQuerySave2>. Each editor that implements <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistDocData.IsDocDataDirty*> must call <xref:Microsoft.VisualStudio.Shell.Interop.IVsQueryEditQuerySave2.QueryEditFiles*> and receive approval to change the document from the environment before returning `True` for `M:Microsoft.VisualStudio.Shell.Interop.IVsPersistDocData.IsDocDataDirty(System.Int32@)`. A project is essentially an editor for a project file, and as a result, has the same responsibility for implementing changed-state tracking for the project file as a text editor does for its files. The environment handles the changed state of the solution, but you must handle the changed state of any object the solution references but does not store, like a project file or its items. In general, if your project or editor is responsible for managing persistence for an item, then it is responsible for implementing changed-state tracking.  
  
 In response to the `IVsQueryEditQuerySave2::QueryEditFiles` call, the environment can do the following:  
  
-   Reject the call to change, in which case the editor or project must remain in the unchanged (clean) state.  
  
-   Indicate that the document data should be reloaded. For a project, the environment will reload the data for the project. An editor must reload the data from disk through its <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistDocData2.ReloadDocData*> implementation. In either case, the context in the project or editor can change when the data is reloaded.  
  
 It is a complex and difficult task to retrofit appropriate `IVsQueryEditQuerySave2::QueryEditFiles` calls onto an existing code base. As a result, these calls should be integrated during the creation of the project or editor.  
  
## Request Permission to Save a File  
 Before a project or editor saves a file, it must call <xref:Microsoft.VisualStudio.Shell.Interop.IVsQueryEditQuerySave2.QuerySaveFile*> or <xref:Microsoft.VisualStudio.Shell.Interop.IVsQueryEditQuerySave2.QuerySaveFiles*>. For project files, these calls are automatically completed by the solution, which knows when to save a project file. Editors are responsible for making these calls unless the editor implementation of `IVsPersistDocData2` uses the helper function <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShell.SaveDocDataToFile*>. If your editor implements `IVsPersistDocData2` in this way, then the call to `IVsQueryEditQuerySave2::QuerySaveFile` or `IVsQueryEditQuerySave2::QuerySaveFiles` is made for you.  
  
> [!NOTE]
>  Always make these calls preemptively—that is, at a time when your editor is able to receive a cancel.  
  
## Request Permission to Add, Remove, or Rename Files in the Project  
 Before a project can add, rename, or remove a file or directory, it must call the appropriate `IVsTrackProjectDocuments2::OnQuery*` method to request permission from the environment. If permission is granted, then the project must complete the operation and then call the appropriate `IVsTrackProjectDocuments2::OnAfter*` method to notify the environment that the operation is complete. The project must call the methods of the <xref:Microsoft.VisualStudio.Shell.Interop.IVsTrackProjectDocuments2> interface for all files (for example, special files) and not just the parent files. File calls are mandatory, but directory calls are optional. If your project has directory information, then it should call the appropriate <xref:Microsoft.VisualStudio.Shell.Interop.IVsTrackProjectDocuments2> methods, but if it does not have this information, then the environment will infer directory information.  
  
 The project should not call the methods of `IVsTrackProjectDocuments2` at project open or close. Listeners that want this information at startup can wait for the <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolutionEvents3.OnAfterOpenSolution*> event and iterate through the solution to find the information they need. On shutdown, this information is not needed. `IVsTrackProjectDocuments2` is provided from the <xref:Microsoft.VisualStudio.Shell.Interop.SVsTrackProjectDocuments>.  
  
 For each add, rename, and remove action, there is an `OnQuery*` method and an `OnAfter*` method. Call the `OnQuery*` method to ask permission to add, rename, or remove the file or directory. Call the `OnAfter*` method after the file or directory has been added, renamed, or removed and the project state reflects the new state.  
  
## See Also  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistDocData>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsQueryEditQuerySave2.QuerySaveFile*>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsQueryEditQuerySave2.QuerySaveFiles*>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsTrackProjectDocuments2>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShell.SaveDocDataToFile*>   
 <xref:Microsoft.VisualStudio.Shell.Interop.SVsTrackProjectDocuments>   
 [Supporting Source Control](../extensibility/supporting-source-control.md)