---
title: "Inside the Core Editor | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "editors [Visual Studio SDK], legacy - core editor"
ms.assetid: 8265f31c-c45b-4858-882c-6d9f1e3b9083
caps.latest.revision: 21
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
# Inside the Core Editor
The [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] core editor is a set of several components that let you modify and query textual information. If you have customized the core editor by using the legacy API, you may continue to use these customizations, which will be routed through editor adapters. It is recommended, however, that you adapt your customizations to the new editor API.  
  
 The following areas are some important aspects of the core editor:  
  
-   Text buffer  
  
-   Text view  
  
-   Code window  
  
-   Text markers  
  
-   Text manager  
  
-   Integration with language services  
  
## In This Section  
 [Instantiating the Core Editor By Using the Legacy API](../extensibility/instantiating-the-core-editor-by-using-the-legacy-api.md)  
 Provides step-by-step instructions about how to use <xref:Microsoft.VisualStudio.Shell.Interop.IVsEditorFactory.CreateEditorInstance%2A> to create an instance of the core editor.  
  
 [Accessing the Text Buffer by Using the Legacy API](../extensibility/accessing-the-text-buffer-by-using-the-legacy-api.md)  
 Discusses the text buffer's role in the core editor, explains the associated systems that are used to access the buffer, and provides a list of the interfaces implemented by the text buffer object, <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextBuffer>.  
  
 [Text Buffer Events in the Legacy API](../extensibility/text-buffer-events-in-the-legacy-api.md)  
 Provides a list of the interfaces that are used for notification of text buffer events.  
  
 [How to: Register for Text Buffer Events with the Legacy API](../extensibility/how-to-register-for-text-buffer-events-with-the-legacy-api.md)  
 Describes how to advise text buffer events.  
  
 [Using the Text Manager to Monitor Global Settings](../extensibility/using-the-text-manager-to-monitor-global-settings.md)  
 Discusses how the text manager is used to share global preference information with the core editor components and how to receive notification of text manager events.  
  
 [Accessing theText View by Using the Legacy API](../extensibility/accessing-thetext-view-by-using-the-legacy-api.md)  
 Describes the text view's role in the core editor and lists the interfaces implemented by the <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextView> object.  
  
 [Customizing Code Windows by Using the Legacy API](../extensibility/customizing-code-windows-by-using-the-legacy-api.md)  
 Provides information about how a code window is used to enclose the text view, discusses how the code window manager is used to provide decorations to the code window, and provides notification of new views.  
  
 [Changing View Settings by Using the Legacy API](../extensibility/changing-view-settings-by-using-the-legacy-api.md)  
 Provides step-by-step instructions about how to force view settings and how to remove forced settings.  
  
 [Language Services and the Core Editor](../extensibility/language-services-and-the-core-editor.md)  
 Describes the instantiation of a language service to control code decorations.  
  
## Related Sections  
 [Walkthrough: Creating a Core Editor and Registering an Editor File Type](../extensibility/walkthrough-creating-a-core-editor-and-registering-an-editor-file-type.md)  
 Provides step-by-step instructions about how to start the core editor from managed code.  
  
 [Drop-down Bar](../extensibility/drop-down-bar.md)  
 Discusses how the drop-down bar is used in the code window and describes the interfaces that are used when you implement a drop-down bar.  
  
 [Using Text Markers with the Legacy API](../extensibility/using-text-markers-with-the-legacy-api.md)  
 Explains the concept of text markers and how they are used in the core editor, and lists the interfaces that are used to access and manage text markers.  
  
 [How to: Add Standard Text Markers](../extensibility/how-to-add-standard-text-markers.md)  
 Provides step-by-step instructions about how to create a text marker and how to add a custom command to a shortcut menu.  
  
 [How to: Create Custom Text Markers](../extensibility/how-to-create-custom-text-markers.md)  
 Provides step-by-step instructions about how to create a custom text marker and how to provide the marker type as a service.