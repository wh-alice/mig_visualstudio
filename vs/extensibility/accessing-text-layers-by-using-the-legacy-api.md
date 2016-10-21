---
title: "Accessing Text Layers by Using the Legacy API | hehe"
ms.custom: ""
ms.date: "10/20/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "editors [Visual Studio SDK], legacy - text layers"
ms.assetid: 2258fcdd-38d1-479d-b8f8-1d4e6525f72c
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
# Accessing Text Layers by Using the Legacy API
A text layer typically encapsulates some aspect of text layout. For example, a "function-at-a-time" layer hides text before and after a function containing the caret (text insertion point).  
  
 A text layer resides between a buffer and a view, and it modifies the way the view sees the buffer's contents.  
  
## Text Layer Information  
 The following list describes how text layers work in [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]:  
  
-   The text in a text layer can be adorned with syntax coloring and markers.  
  
-   You currently cannot implement your own layers.  
  
-   A layer exposes <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLayer>, which is derived from <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLines>. The text buffer itself is also implemented as a layer, which enables a view to deal polymorphically with underlying layers.  
  
-   Any number of layers may lie between the view and the buffer. Each layer deals only with the layer below it, and the view deals largely with the top-most layer. (The view does have some information about the buffer.)  
  
-   A layer can affect only layers that are below it. It cannot affect the layers above it beyond originating standard events.  
  
-   In the editor, hidden text, synthetic text, and word wrap are implemented as layers. You can implement hidden and synthetic text without interacting directly with the layers. For more information, see [Outlining in a Legacy Language Service](../extensibility-internals/outlining-in-a-legacy-language-service.md) and <xref:Microsoft.VisualStudio.TextManager.Interop.IVsSyntheticTextSession>.  
  
-   Each text layer has its own local coordinate system that is exposed through the <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLayer> interface. The line-wrap layer, for example, might contain two lines while the underlying text buffer might contain only one line.  
  
-   The view communicates to layers through the <xref:Microsoft.VisualStudio.TextManager.Interop.IVsLayeredTextView> interface. Use this interface to reconcile view coordinates with buffer coordinates.  
  
-   Any layer such as the synthetic text layer that originates text must provide a local implementation of <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLayer.CreateTrackingPoint*>.  
  
-   Besides <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLayer>, a text layer must implement <xref:Microsoft.VisualStudio.OLE.Interop.IConnectionPointContainer> and fire the events in the <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLinesEvents> interface.  
  
## See Also  
 [Syntax Coloring in Custom Editors](../extensibility/syntax-coloring-in-custom-editors.md)   
 [Using Text Markers with the Legacy API](../extensibility/using-text-markers-with-the-legacy-api.md)   
 [Customizing Editor Controls and Menus by Using the Legacy API](../extensibility/customizing-editor-controls-and-menus-by-using-the-legacy-api.md)