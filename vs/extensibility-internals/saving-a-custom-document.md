---
title: "Saving a Custom Document | testtitle"
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
  - "persistence, saving custom documents"
  - "projects [Visual Studio SDK], saving custom documents"
  - "editors [Visual Studio SDK], saving custom documents"
ms.assetid: 040b36d6-1f0a-4579-971c-40fbb46ade1d
caps.latest.revision: 12
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
# Saving a Custom Document
The environment handles the **Save**, **Save As**, and **Save All** commands. When a user clicks **Save**, **Save As**, **or Save All** on the **File** menu or closes the solution, resulting in a Save All, the following process occurs.  
  
 ![Customer Editor Save](../extensibility-internals/media/private.gif "Private")  
Save, Save As, and Save All command handling for a custom editor  
  
 This process is detailed in the following steps:  
  
1.  For the **Save** and **Save As** commands, the environment uses the <xref:Microsoft.VisualStudio.Shell.Interop.SVsShellMonitorSelection> service to determine the active document window and thus what items should be saved. Once the active document window is known, the environment finds the hierarchy pointer and item identifier (itemID) for the document in the running document table. For more information, see [Running Document Table](../extensibility-internals/running-document-table.md).  
  
     For the Save All command, the environment uses the information in the running document table to compile the list of all items to save.  
  
2.  When the solution receives an <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget.QueryStatus*> call, it iterates through the set of selected items (that is, the multiple selections exposed by the <xref:Microsoft.VisualStudio.Shell.Interop.SVsShellMonitorSelection> service).  
  
3.  On each item in the selection, the solution uses the hierarchy pointer to call the <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistHierarchyItem2.IsItemDirty*> method to determine whether the Save menu command should be enabled. If one or more items are dirty, then the Save command is enabled. If the hierarchy uses a standard editor, then the hierarchy delegates querying for dirty status to the editor by calling the <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistDocData2.IsDocDataDirty*> method.  
  
4.  On each selected item that is dirty, the solution uses the hierarchy pointer to call the <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistHierarchyItem2.SaveItem*> method on the appropriate hierarchies.  
  
     In the case of a custom editor, the communication between the document data object and the project is private. Thus, any special persistence concerns are handled between these two objects.  
  
    > [!NOTE]
    >  If you implement your own persistence, be sure to call the <xref:Microsoft.VisualStudio.Shell.Interop.IVsQueryEditQuerySave2.QuerySaveFiles*> method to save time. This method checks to make sure that it is safe to save the file (for example, the file is not read-only).  
  
## See Also  
 <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget>   
 [Opening and Saving Project Items](../extensibility-internals/opening-and-saving-project-items.md)