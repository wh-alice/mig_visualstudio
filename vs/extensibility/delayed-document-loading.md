---
title: "Delayed Document Loading"
ms.custom: ""
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: fb07b8e2-a4e3-4cb0-b04f-8eb11c491f35
caps.latest.revision: 6
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
# Delayed Document Loading
When a user reopens a Visual Studio solution, most of the associated documents are not loaded immediately. The document window frame is created in a pending-initialization state, and a placeholder document (called a stub frame) is placed in the Running Document Table (RDT).  
  
 Your extension may cause project documents to be loaded unnecessarily by querying elements in the documents before they are loaded. This can increase the overall memory footprint for Visual Studio.  
  
## Document Loading  
 The stub frame and document are fully initialized when the user accesses the document, for example by selecting the tab of the window frame. The document can also be initialized by an extension that requests the document’s data, either by accessing the RDT directly to acquire the document data, or accessing the RDT indirectly by making one of the following calls:  
  
-   The window frame show method: <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowFrame.Show*>.  
  
-   The window frame GetProperty method <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowFrame.GetProperty*> on any of the following properties:  
  
    -   <xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID>  
  
    -   <xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID>  
  
    -   <xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID>  
  
    -   <xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID>  
  
    -   <xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID>  
  
    -   <xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID>  
  
 If your extension uses managed code, you should not call <xref:Microsoft.VisualStudio.Shell.Interop.IVsRunningDocumentTable.GetDocumentInfo*> unless you are certain that the document is not in the pending-initialization state, or you want the document to be fully initialized.. This is because this method always returns the doc data object, creating it if necessary. Instead, you should call one of the methods on the IVsRunningDocumentTable4 interface.  
  
 If your extension uses C++, you can pass `null` for the parameters you don’t want.  
  
 You can avoid unnecessary document loading by calling one of the following methods before you ask for the relevant properties: before you ask for other properties.  
  
-   <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowFrame.GetProperty*> using <xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID6>.  
  
-   <xref:Microsoft.VisualStudio.Shell.Interop.IVsRunningDocumentTable4.GetDocumentFlags*>. This method returns a <xref:Microsoft.VisualStudio.Shell.Interop._VSRDTFLAGS4> object that includes a value for <xref:Microsoft.VisualStudio.Shell.Interop._VSRDTFLAGS4> if the document has not yet been initialized.  
  
 You can find out when a document has been loaded by subscribing to the RDT event that is raised when a document is fully initialized. There are two possibilities:  
  
-   If the event sink implements <xref:Microsoft.VisualStudio.Shell.Interop.IVsRunningDocTableEvents2>, you can subscribe to <xref:Microsoft.VisualStudio.Shell.Interop.IVsRunningDocTableEvents2.OnAfterAttributeChangeEx*>,  
  
-   Otherwise, you can subscribe to <xref:Microsoft.VisualStudio.Shell.Interop.IVsRunningDocTableEvents.OnAfterAttributeChange*>.  
  
 The following is a hypothetical document access scenario. A Visual Studio extension want to display some information about open documents, for instance the edit lock count and something about the document data. It enumerates the documents in the RDT using <xref:Microsoft.VisualStudio.Shell.Interop.IEnumRunningDocuments>, then calls <xref:Microsoft.VisualStudio.Shell.Interop.IVsRunningDocumentTable.GetDocumentInfo*> for each document in order to retrieve the edit lock count and document data. If the document is in the pending-initialization state, requesting the document data causes it to be unnecessarily initialized.  
  
 A more efficient way of doing this is to use <xref:Microsoft.VisualStudio.Shell.Interop.IVsRunningDocumentTable4.GetDocumentEditLockCount*> to get the edit lock count, and then use <xref:Microsoft.VisualStudio.Shell.Interop.IVsRunningDocumentTable4.GetDocumentFlags*> to determine whether the document has been initialized. If the flags do not include <xref:Microsoft.VisualStudio.Shell.Interop._VSRDTFLAGS4>, the document has already been initialized ,and requesting the document data with <xref:Microsoft.VisualStudio.Shell.Interop.IVsRunningDocumentTable4.GetDocumentData*> does not cause any unnecessary initialization. If the flags do include <xref:Microsoft.VisualStudio.Shell.Interop._VSRDTFLAGS4>, the extension should avoid requesting the document data until the document is initialized. This can be detected in the OnAfterAttributeChange(Ex) event handler.  
  
## Testing extensions to see if they force initialization  
 There is no visible cue to indicate whether a document has been initialized, so it can be difficult to find out if your extension is forcing initialization. You can set a registry key that makes verification easier, because it causes the title of every document that is not fully initialized to have the text `[Stub]` in the title.  
  
 In **HKEY_CURRENT_USER\Software\Microsoft\VisualStudio\14.0\BackgroundSolutionLoad]**, set **StubTabTitleFormatString** to **{0} [Stub]**.