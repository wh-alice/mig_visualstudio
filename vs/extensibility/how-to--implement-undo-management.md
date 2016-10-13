---
title: "How to: Implement Undo Management"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "editors [Visual Studio SDK], legacy - undo management"
ms.assetid: 1942245d-7a1d-4a11-b5e7-a3fe29f11c0b
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
# How to: Implement Undo Management
The primary interface used for undo management is \<xref:Microsoft.VisualStudio.OLE.Interop.IOleUndoManager>, which is implemented by the environment. To support undo management, implement separate undo units (that is, \<xref:Microsoft.VisualStudio.OLE.Interop.IOleUndoUnit>, which can contain multiple individual steps.  
  
 How you implement undo management varies depending on whether your editor supports multiple views or not. The procedures for each implementation are detailed in the following sections.  
  
## Cases where an editor supports a single view  
 In this scenario, the editor does not support multiple views. There is only one editor and one document, and they support undo. Use the following procedure to implement undo management.  
  
#### To support undo management for a single-view editor  
  
1.  Call `QueryInterface` on the `IServiceProvider` interface on the window frame for `IOleUndoManager`, from the document view object to access the undo manager (`IID_IOLEUndoManager`).  
  
2.  When a view is sited into a window frame, it gets a site pointer, which it can use to call `QueryInterface` for `IServiceProvider`.  
  
## Cases where an editor supports multiple views  
 If you have document and view separation, then there is normally one undo manager associated with the document itself. All undo units are placed on one undo manager associated with the document data object.  
  
 Instead of the view querying for the undo manager, of which there is one for each view, the document data object calls \<xref:Microsoft.VisualStudio.Shell.Interop.ILocalRegistry2.CreateInstance*> to instantiate the undo manager, specifying a class identifier of CLSID_OLEUndoManager. The class identifier is defined in the OCUNDOID.h file.  
  
 When using \<xref:Microsoft.VisualStudio.Shell.Interop.ILocalRegistry2.CreateInstance*> to create your own undo manager instance, use the following procedure to hook your undo manager into the environment.  
  
#### To hook your undo manager into the environment  
  
1.  Call `QueryInterface` on the object returned from \<xref:Microsoft.VisualStudio.Shell.Interop.ILocalRegistry2> for `IID_IOleUndoManager`. Store the pointer to \<xref:Microsoft.VisualStudio.OLE.Interop.IOleUndoManager>.  
  
2.  Call `QueryInterface` on `IOleUndoManager` for `IID_IOleCommandTarget`. Store the pointer to \<xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget>.  
  
3.  Relay your \<xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget.QueryStatus*> and \<xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget.Exec*> calls into the stored `IOleCommandTarget` interface for the following StandardCommandSet97 commands:  
  
    -   cmdidUndo  
  
    -   cmdidMultiLevelUndo  
  
    -   cmdidRedo  
  
    -   cmdidMultiLevelRedo  
  
    -   cmdidMultiLevelUndoList  
  
    -   cmdidMultiLevelRedoList  
  
4.  Call `QueryInterface` on `IOleUndoManager` for `IID_IVsChangeTrackingUndoManager`. Store the pointer to \<xref:Microsoft.VisualStudio.TextManager.Interop.IVsChangeTrackingUndoManager>.  
  
     Use the pointer to \<xref:Microsoft.VisualStudio.TextManager.Interop.IVsChangeTrackingUndoManager> to call the \<xref:Microsoft.VisualStudio.TextManager.Interop.IVsChangeTrackingUndoManager.MarkCleanState*>, the \<xref:Microsoft.VisualStudio.TextManager.Interop.IVsChangeTrackingUndoManager.AdviseTrackingClient*>, and the \<xref:Microsoft.VisualStudio.TextManager.Interop.IVsChangeTrackingUndoManager.UnadviseTrackingClient*> methods.  
  
5.  Call `QueryInterface` on `IOleUndoManager` for `IID_IVsLinkCapableUndoManager`.  
  
6.  Call \<xref:Microsoft.VisualStudio.TextManager.Interop.IVsLinkCapableUndoManager.AdviseLinkedUndoClient*> with your document, which should also implement the \<xref:Microsoft.VisualStudio.TextManager.Interop.IVsLinkedUndoClient> interface. When your document is closed, call `IVsLinkCapableUndoManager::UnadviseLinkedUndoClient`.  
  
7.  When your document is closed, call `QueryInterface` on your undo manager for `IID_IVsLifetimeControlledObject`.  
  
8.  Call \<xref:Microsoft.VisualStudio.TextManager.Interop.IVsLifetimeControlledObject.SeverReferencesToOwner*>.  
  
9. When changes are made to the document, call \<xref:Microsoft.VisualStudio.OLE.Interop.IOleUndoManager.Add*> on the manager with an `OleUndoUnit` class. The \<xref:Microsoft.VisualStudio.OLE.Interop.IOleUndoManager.Add*> method keeps a reference to the object, so generally you release it right after the \<xref:Microsoft.VisualStudio.OLE.Interop.IOleUndoManager.Add*>.  
  
 The `OleUndoManager` class represents a single undo stack instance. Thus, there is one undo manager object per data entity being tracked for undo or redo.  
  
> [!NOTE]
>  While the undo manager object is used extensively by the text editor, it is a general component that has no specific support for the text editor. If you want to support multi-level undo or redo, you can use this object to do so.  
  
## See Also  
 \<xref:Microsoft.VisualStudio.TextManager.Interop.IVsChangeTrackingUndoManager>   
 \<xref:Microsoft.VisualStudio.TextManager.Interop.IVsLifetimeControlledObject>   
 [How to: Clear the Undo Stack](../extensibility/how-to--clear-the-undo-stack.md)