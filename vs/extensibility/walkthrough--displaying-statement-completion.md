---
title: "Walkthrough: Displaying Statement Completion | Microsoft Docs"
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
  - "editors [Visual Studio SDK], new - statement completion"
ms.assetid: f3152c4e-7673-4047-a079-2326941d1c83
caps.latest.revision: 36
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
# Walkthrough: Displaying Statement Completion
You can implement language-based statement completion by defining the identifiers for which you want to provide completion and then triggering a completion session. You can define statement completion in the context of a language service, define your own file name extension and content type and then display completion for just that type, or you can trigger completion for an existing content type—for example, "plaintext". This walkthrough shows how to trigger statement completion for the "plaintext" content type, which is the content type of text files. The "text" content type is the ancestor of all other content types, including code and XML files.  
  
 Statement completion is typically triggered by typing certain characters—for example, by typing the beginning of an identifier such as "using". It is typically dismissed by pressing the Spacebar, Tab, or Enter key to commit a selection. You can implement the IntelliSense features that are triggered by typing a character by using a command handler for the keystrokes (the <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget> interface) and a handler provider that implements the <xref:Microsoft.VisualStudio.Editor.IVsTextViewCreationListener> interface. To create the completion source, which is the list of identifiers that participate in completion, implement the <xref:Microsoft.VisualStudio.Language.Intellisense.ICompletionSource> interface and a completion source provider (the <xref:Microsoft.VisualStudio.Language.Intellisense.ICompletionSourceProvider> interface). The providers are Managed Extensibility Framework (MEF) component parts. They are responsible for exporting the source and controller classes and importing services and brokers—for example, the <xref:Microsoft.VisualStudio.Text.Operations.ITextStructureNavigatorSelectorService>, which enables navigation in the text buffer, and the <xref:Microsoft.VisualStudio.Language.Intellisense.ICompletionBroker>, which triggers the completion session.  
  
 This walkthrough shows how to implement statement completion for a hard-coded set of identifiers. In full implementations, the language service and the language documentation are responsible for providing that content.  
  
## Prerequisites  
 Starting in Visual Studio 2015, you do not install the Visual Studio SDK from the download center. It is included as an optional feature in Visual Studio setup. You can also install the VS SDK later on. For more information, see [Installing the Visual Studio SDK](../extensibility/installing-the-visual-studio-sdk.md).  
  
## Creating a MEF Project  
  
#### To create a MEF project  
  
1.  Create a C# VSIX project. (In the **New Project** dialog, select **Visual C# / Extensibility**, then **VSIX Project**.) Name the solution `CompletionTest`.  
  
2.  Add an Editor Classifier item template to the project. For more information, see [Creating an Extension with an Editor Item Template](../extensibility/creating-an-extension-with-an-editor-item-template.md).  
  
3.  Delete the existing class files.  
  
4.  Add the following references to the project and make sure that **CopyLocal** is set to `false`:  
  
     Microsoft.VisualStudio.Editor  
  
     Microsoft.VisualStudio.Language.Intellisense  
  
     Microsoft.VisualStudio.OLE.Interop  
  
     Microsoft.VisualStudio.Shell.14.0  
  
     Microsoft.VisualStudio.Shell.Immutable.10.0  
  
     Microsoft.VisualStudio.TextManager.Interop  
  
## Implementing the Completion Source  
 The completion source is responsible for collecting the set of identifiers and adding the content to the completion window when a user types a completion trigger, such as the first letters of an identifier. In this example, the identifiers and their descriptions are hard-coded in the <xref:Microsoft.VisualStudio.Language.Intellisense.ICompletionSource.AugmentCompletionSession*> method. In most real-world uses, you would use your language’s parser to get the tokens to populate the completion list.  
  
#### To implement the completion source  
  
1.  Add a class file and name it `TestCompletionSource`.  
  
2.  Add these imports:  
  
     [!CODE [VSSDKCompletionTest#1](../CodeSnippet/VS_Snippets_VSSDK/vssdkcompletiontest#1)]  
  
3.  Modify the class declaration for `TestCompletionSource` so that it implements <xref:Microsoft.VisualStudio.Language.Intellisense.ICompletionSource>:  
  
     [!CODE [VSSDKCompletionTest#2](../CodeSnippet/VS_Snippets_VSSDK/vssdkcompletiontest#2)]  
  
4.  Add private fields for the source provider, the text buffer, and a list of <xref:Microsoft.VisualStudio.Language.Intellisense.Completion> objects (which correspond to the identifiers that will participate in the completion session):  
  
     [!CODE [VSSDKCompletionTest#3](../CodeSnippet/VS_Snippets_VSSDK/vssdkcompletiontest#3)]  
  
5.  Add a constructor that sets the source provider and buffer. The `TestCompletionSourceProvider` class is defined in later steps:  
  
     [!CODE [VSSDKCompletionTest#4](../CodeSnippet/VS_Snippets_VSSDK/vssdkcompletiontest#4)]  
  
6.  Implement the <xref:Microsoft.VisualStudio.Language.Intellisense.ICompletionSource.AugmentCompletionSession*> method by adding a completion set that contains the completions you want to provide in the context. Each completion set contains a set of <xref:Microsoft.VisualStudio.Language.Intellisense.Completion> completions, and corresponds to a tab of the completion window. (In Visual Basic projects, the completion window tabs are named **Common** and **All**.) The FindTokenSpanAtPosition method is defined in the next step.  
  
     [!CODE [VSSDKCompletionTest#5](../CodeSnippet/VS_Snippets_VSSDK/vssdkcompletiontest#5)]  
  
7.  The following method is used to find the current word from the position of the cursor:  
  
     [!CODE [VSSDKCompletionTest#6](../CodeSnippet/VS_Snippets_VSSDK/vssdkcompletiontest#6)]  
  
8.  Implement the `Dispose()` method:  
  
     [!CODE [VSSDKCompletionTest#7](../CodeSnippet/VS_Snippets_VSSDK/vssdkcompletiontest#7)]  
  
## Implementing the Completion Source Provider  
 The completion source provider is the MEF component part that instantiates the completion source.  
  
#### To implement the completion source provider  
  
1.  Add a class named `TestCompletionSourceProvider` that implements <xref:Microsoft.VisualStudio.Language.Intellisense.ICompletionSourceProvider>. Export this class with a <xref:Microsoft.VisualStudio.Utilities.ContentTypeAttribute> of "plaintext" and a <xref:Microsoft.VisualStudio.Utilities.NameAttribute> of "test completion".  
  
     [!CODE [VSSDKCompletionTest#8](../CodeSnippet/VS_Snippets_VSSDK/vssdkcompletiontest#8)]  
  
2.  Import a <xref:Microsoft.VisualStudio.Text.Operations.ITextStructureNavigatorSelectorService>, which is used to find the current word in the completion source.  
  
     [!CODE [VSSDKCompletionTest#9](../CodeSnippet/VS_Snippets_VSSDK/vssdkcompletiontest#9)]  
  
3.  Implement the <xref:Microsoft.VisualStudio.Language.Intellisense.ICompletionSourceProvider.TryCreateCompletionSource*> method to instantiate the completion source.  
  
     [!CODE [VSSDKCompletionTest#10](../CodeSnippet/VS_Snippets_VSSDK/vssdkcompletiontest#10)]  
  
## Implementing the Completion Command Handler Provider  
 The completion command handler provider is derived from a <xref:Microsoft.VisualStudio.Editor.IVsTextViewCreationListener>, which listens for a text view creation event and converts the view from an <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView>—which enables the addition of the command to the command chain of the Visual Studio shell—to an <xref:Microsoft.VisualStudio.Text.Editor.ITextView>. Because this class is a MEF export, you can also use it to import the services that are required by the command handler itself.  
  
#### To implement the completion command handler provider  
  
1.  Add a file named `TestCompletionCommandHandler`.  
  
2.  Add these using statements:  
  
     [!CODE [VSSDKCompletionTest#11](../CodeSnippet/VS_Snippets_VSSDK/vssdkcompletiontest#11)]  
  
3.  Add a class named `TestCompletionHandlerProvider` that implements <xref:Microsoft.VisualStudio.Editor.IVsTextViewCreationListener>. Export this class with a <xref:Microsoft.VisualStudio.Utilities.NameAttribute> of "token completion handler", a <xref:Microsoft.VisualStudio.Utilities.ContentTypeAttribute> of "plaintext", and a <xref:Microsoft.VisualStudio.Text.Editor.TextViewRoleAttribute> of <xref:Microsoft.VisualStudio.Text.Editor.PredefinedTextViewRoles.Editable>.  
  
     [!CODE [VSSDKCompletionTest#12](../CodeSnippet/VS_Snippets_VSSDK/vssdkcompletiontest#12)]  
  
4.  Import the <xref:Microsoft.VisualStudio.Editor.IVsEditorAdaptersFactoryService>, which enables conversion from a <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView> to a <xref:Microsoft.VisualStudio.Text.Editor.ITextView>, a <xref:Microsoft.VisualStudio.Language.Intellisense.ICompletionBroker>, and a <xref:Microsoft.VisualStudio.Shell.SVsServiceProvider> that enables access to standard Visual Studio services.  
  
     [!CODE [VSSDKCompletionTest#13](../CodeSnippet/VS_Snippets_VSSDK/vssdkcompletiontest#13)]  
  
5.  Implement the <xref:Microsoft.VisualStudio.Editor.IVsTextViewCreationListener.VsTextViewCreated*> method to instantiate the command handler.  
  
     [!CODE [VSSDKCompletionTest#14](../CodeSnippet/VS_Snippets_VSSDK/vssdkcompletiontest#14)]  
  
## Implementing the Completion Command Handler  
 Because statement completion is triggered by keystrokes, you must implement the <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget> interface to receive and process the keystrokes that trigger, commit, and dismiss the completion session.  
  
#### To implement the completion command handler  
  
1.  Add a class named `TestCompletionCommandHandler` that implements <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget>:  
  
     [!CODE [VSSDKCompletionTest#15](../CodeSnippet/VS_Snippets_VSSDK/vssdkcompletiontest#15)]  
  
2.  Add private fields for the next command handler (to which you pass the command), the text view, the command handler provider (which enables access to various services), and a completion session:  
  
     [!CODE [VSSDKCompletionTest#16](../CodeSnippet/VS_Snippets_VSSDK/vssdkcompletiontest#16)]  
  
3.  Add a constructor that sets the text view and the provider fields, and adds the command to the command chain:  
  
     [!CODE [VSSDKCompletionTest#17](../CodeSnippet/VS_Snippets_VSSDK/vssdkcompletiontest#17)]  
  
4.  Implement the <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget.QueryStatus*> method by passing the command along:  
  
     [!CODE [VSSDKCompletionTest#18](../CodeSnippet/VS_Snippets_VSSDK/vssdkcompletiontest#18)]  
  
5.  Implement the <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget.Exec*> method. When this method receives a keystroke, it must do one of these things:  
  
    -   Allow the character to be written to the buffer, and then trigger or filter completion. (Printing characters do this.)  
  
    -   Commit the completion, but do not allow the character to be written to the buffer. (Whitespace, Tab, and Enter do this when a completion session is displayed.)  
  
    -   Allow the command to be passed on to the next handler. (All other commands.)  
  
     Because this method may display UI, call <xref:Microsoft.VisualStudio.Shell.VsShellUtilities.IsInAutomationFunction*> to make sure that it is not called in an automation context:  
  
     [!CODE [VSSDKCompletionTest#19](../CodeSnippet/VS_Snippets_VSSDK/vssdkcompletiontest#19)]  
  
6.  This code is a private method that triggers the completion session:  
  
     [!CODE [VSSDKCompletionTest#20](../CodeSnippet/VS_Snippets_VSSDK/vssdkcompletiontest#20)]  
  
7.  The next example is a private method that unsubscribes from the <xref:Microsoft.VisualStudio.Language.Intellisense.IIntellisenseSession.Dismissed> event:  
  
     [!CODE [VSSDKCompletionTest#21](../CodeSnippet/VS_Snippets_VSSDK/vssdkcompletiontest#21)]  
  
## Building and Testing the Code  
 To test this code, build the CompletionTest solution and run it in the experimental instance.  
  
#### To build and test the CompletionTest solution  
  
1.  Build the solution.  
  
2.  When you run this project in the debugger, a second instance of Visual Studio is instantiated.  
  
3.  Create a text file and type some text that includes the word "add".  
  
4.  As you type first "a" and then "d", a list that contains "addition" and "adaptation" should be displayed. Notice that addition is selected. When you type another "d", the list should contain only "addition", which is now selected. You can commit "addition" by pressing the Spacebar, Tab, or Enter key, or dismiss the list by typing Esc or any other key.  
  
## See Also  
 [Walkthrough: Linking a Content Type to a File Name Extension](../extensibility/walkthrough--linking-a-content-type-to-a-file-name-extension.md)