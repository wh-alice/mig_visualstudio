---
title: "New or Changed Behavior with Editor Adapters | hehe"
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
  - "editors [Visual Studio SDK], legacy - adapter behavior"
ms.assetid: 5555b116-cfdb-4773-ba62-af80fda64abd
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
# New or Changed Behavior with Editor Adapters
If you are updating code that was written against earlier versions of the Visual Studio core editor, and you plan to use the editor adapters (or shims) rather than using the new API, you should be aware of the following differences in the behavior of the editor adapters with respect to the previous core editor.  
  
## Features  
  
#### Using SetSite()  
 You must call <xref:Microsoft.VisualStudio.OLE.Interop.IObjectWithSite.SetSite*> when you CoCreate text buffers, text views, and code windows before you perform any other operations on them. However, this is not necessary if you use the <xref:Microsoft.VisualStudio.Editor.IVsEditorAdaptersFactoryService> to create them, because this service's Create() methods themselves call <xref:Microsoft.VisualStudio.Shell.Interop.IVsEditorFactory.SetSite*>.  
  
#### Hosting IVsCodeWindow and IVsTextView in your own content  
 You can host both <xref:Microsoft.VisualStudio.TextManager.Interop.IVsCodeWindow> and <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView> in your own content using either Win32 mode or WPF mode. However, you should keep in mind that there are some differences in the two modes.  
  
##### Using Win32 and WPF versions of IVsCodeWindow  
 The editor code window is derived from <xref:Microsoft.VisualStudio.Shell.WindowPane>, which implements the older Win32 <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowPane> interface as well as the new WPF <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIElementPane> interface. You can use the <xref:Microsoft.VisualStudio.Shell.WindowPane.Microsoft#VisualStudio#Shell#Interop#IVsWindowPane#CreatePaneWindow*> method to create an HWND-based hosting environment, or the <xref:Microsoft.VisualStudio.Shell.WindowPane.Microsoft#VisualStudio#Shell#Interop#IVsUIElementPane#CreateUIElementPane*> method to create a WPF hosting environment. The underlying editor always uses WPF, but you can create the kind of window pane that suits your hosting requirements if you are embedding this window pane directly into your own content.  
  
##### Using Win32 and WPF versions of IVsTextView  
 You can set an <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView> to Win32 mode or WPF mode.  
  
 When an editor factory creates a text view, by default it is hosted inside an HWND, and <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView.GetWindowHandle*> returns an HWND. You should not use this mode to embed the editor inside a WPF control.  
  
 To set a text view to WPF mode, you must call <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView.Initialize*> and pass in <xref:Microsoft.VisualStudio.TextManager.Interop.TextViewInitFlags3> as one of the initialization flags in the `InitView` parameter. You can get the <xref:System.Windows.FrameworkElement> by calling <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIElementPane.CreateUIElementPane*>.  
  
 WPF mode differs from Win32 mode in two ways. First, the text view can be hosted in a WPF context. You can access the WPF pane by casting the <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView> to <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIElementPane> and calling <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIElement.GetUIObject*>. Second, <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView.GetWindowHandle*> still returns an HWND, but this HWND can be used only to check its position and set focus on it. You must not use this HWND to respond to a WM_PAINT message, because it will not affect how the editor paints the window. This HWND is present only to facilitate the transition to the new editor code by means of the adapters. It is highly recommended that you should not use `VIF_NO_HWND_SUPPORT` if your component requires an HWND to work, due to the limitations in the HWND returned from `GetWindowHandle` while in this mode.  
  
#### Passing arrays as parameters in native code  
 There are many methods in the legacy editor API that have parameters that include an array and its count. Examples are:  
  
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextViewEx.AppendViewOnlyMarkerTypes*>  
  
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextViewEx.RemoveViewOnlyMarkerTypes*>  
  
 If you are calling these methods in native code, you must pass in only one element at a time. If you pass in more than one element, the call will be rejected, due to problems with the primary interop implementation.  
  
 The problem is more complex with methods such as <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextViewEx.SetIgnoreMarkerTypes*>. Every time this method is called, it clears the previous list of ignored marker types, so it is not possible simply to call this method three times with three different marker types. The only remedy is to call this method only in managed code.  
  
#### Threading  
 You should always call the buffer adapter from the UI thread. The buffer adapter is a managed object, which means that calling into it from managed code will bypass COM marshaling and your call will not automatically be marshaled to the UI thread.  If you are calling the buffer adapter from a background thread, you must use <xref:System.Windows.Threading.Dispatcher.Invoke*> or a similar method.  
  
#### LockBuffer methods  
 All LockBuffer() methods are deprecated. Examples are:  
  
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextBuffer.LockBuffer*>  
  
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextStream.LockBuffer*>  
  
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLines.LockBuffer*>  
  
#### Commit events  
 Commit events are not supported. Calling a method that advises for these events causes the method to return a failure code.  
  
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsPreliminaryTextChangeCommitEvents>  
  
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFinalTextChangeCommitEvents>  
  
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsUndoRedoClusterWithCommitEvents>  
  
#### TextEditorEvents  
 The <xref:EnvDTE.TextEditorEvents> no longer fire on Commit(). Instead they fire on every text change.  
  
#### Text Markers  
 You must call <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextMarker.Invalidate*> on <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextMarker> objects when you remove them. In previous versions, you needed only to release the markers.  
  
#### Line numbers  
 For a variety of methods on <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView> and <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextViewEx>, line numbers correspond to underlying buffer line numbers, not line numbers that factor in outlining and word-wrap, as in Visual Studio 2008.  
  
 The methods affected include the following (the list is not exhaustive):  
  
-   <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView.CenterLines*>  
  
-   <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView.GetCaretPos*>  
  
-   <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView.GetLineAndColumn*>  
  
-   <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView.GetNearestPosition*>  
  
-   <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView.GetPointOfLineColumn*>  
  
-   <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView.GetTextStream*>  
  
-   <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView.GetWordExtent*>  
  
-   <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView.PositionCaretForEditing*>  
  
-   <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView.ReplaceTextOnLine*>  
  
-   <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView.SetCaretPos*>  
  
-   <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView.SetSelection*>  
  
-   <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView.SetTopLine*>  
  
#### Outlining  
 Clients of <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextSession> will see only those outlining regions that were added using <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextSession.AddHiddenRegions*>or <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextSessionEx.AddHiddenRegionsEx*>. They will not see ad hoc regions, because they are not added through the editor adapters. Likewise, these clients will not see outlining regions added by languages (including C# and C++) that are using the new editor code rather than the editor adapters.  
  
#### Line heights  
 In the new editor, text lines can have different heights, depending on the font size and possible line transforms that may move the line relative to other lines. The line height returned by methods such as <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView.GetLineHeight*> is the height of a line using the default font size with no line transforms applied. This height may or may not reflect the actual height of a line in the view.  
  
#### Eventing and undo  
 In the new editor, the view continues to perform operations such as rendering and raising events continuously, even when an undo cluster is open. This behavior is different from that of legacy views, which did not perform those operations until after the closing of the undo cluster.  
  
#### IntelliSense  
  
-   The <xref:Microsoft.VisualStudio.TextManager.Interop.IVsIntellisenseHost.UpdateTipWindow*> method will fail if you pass in a class that does not implement either <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextTipWindow2> or <xref:Microsoft.VisualStudio.TextManager.Interop.IVsMethodTipWindow3>. Custom Win32 owner-drawn popups are no longer supported.  
  
#### SmartTags  
 There is no adapter support for smart tags created with, <xref:Microsoft.VisualStudio.TextManager.Interop.IVsSmartTagData>, <xref:Microsoft.VisualStudio.TextManager.Interop.IVsSmartTagTipWindow>, and <xref:Microsoft.VisualStudio.TextManager.Interop.IVsSmartTagTipWindow2> interfaces.  
  
#### DTE  
 <xref:EnvDTE80.IncrementalSearch> is not implemented.  
  
## Unimplemented methods  
 Some methods have not been implemented on the text buffer adapter, text view adapter, and text layer adapter.  
  
|Interface|Not implemented|  
|---------------|---------------------|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextBuffer>|`Reload(false)` is not implemented.|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextBufferCoordinator>|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextBufferCoordinator.EnumSpans*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextBufferCoordinator.SetBufferMappingModes*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextBufferCoordinator.SetSpanMappings*>|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLines>|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLines.GetMarkerData*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLines.ReleaseMarkerData*>|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLayer>|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLayer.CanReplaceLines*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLayer.CopyLineText*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLayer.CreateTrackingPoint*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLayer.EnumLayerMarkers*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLayer.GetBaseBuffer*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLayer.GetLengthOfLine*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLayer.GetLineCount*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLayer.GetLineText*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLayer.GetMarkerData*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLayer.LockBufferEx*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLayer.MapLocalSpansToTextOriginatingLayer*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLayer.ReleaseMarkerData*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLayer.ReplaceLines*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLayer.ReplaceLinesEx*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLayer.UnlockBufferEx*>|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget>|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Find*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Replace*>|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsLayeredTextView>|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsLayeredTextView.GetSelectedAtom*>|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView>|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView.GetSelectionDataObject*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView.PositionCaretForEditing*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView.RestrictViewRange*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView.UpdateViewFrameCaption*>|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextViewEx>|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextViewEx.GetSmartTagRect*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextViewEx.InvokeInsertionUI*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextViewEx.SetHoverWaitTimer*>|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsCodeWindow>|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsCodeWindow.SetViewClassID*>|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsIntellisenseHost>|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsIntellisenseHost.AfterCompletorCommit*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsIntellisenseHost.BeforeCompletorCommit*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsIntellisenseHost.Exec*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsIntellisenseHost.GetContextLocation*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsIntellisenseHost.GetServiceProvider*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsIntellisenseHost.GetSmartTagRect*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsIntellisenseHost.GetSubjectCaretPos*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsIntellisenseHost.GetSubjectSelection*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsIntellisenseHost.GetSubjectText*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsIntellisenseHost.QueryStatus*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsIntellisenseHost.ReplaceSubjectTextSpan*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsIntellisenseHost.SetSubjectCaretPos*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsIntellisenseHost.SetSubjectSelection*><br /><br /> <xref:Microsoft.VisualStudio.TextManager.Interop.IVsIntellisenseHost.UpdateSmartTagWindow*>|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextViewIntellisenseHost>|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextViewIntellisenseHost.SetSubjectFromPrimaryBuffer*> is implemented in the adapters but ignored by the outlining UI.|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenRegionEx>|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenRegionEx.GetBannerAttr*> is implemented in the adapters but ignored by the outlining UI.|