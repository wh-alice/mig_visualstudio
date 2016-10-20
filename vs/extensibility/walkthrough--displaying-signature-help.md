---
title: "Walkthrough: Displaying Signature Help | Microsoft Docs"
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
  - "editors [Visual Studio SDK], new - signature help/parameter info"
ms.assetid: 4a6a884b-5730-4b54-9264-99684f5b523c
caps.latest.revision: 28
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
# Walkthrough: Displaying Signature Help
Signature Help (also known as *Parameter Info*) displays the signature of a method in a tooltip when a user types the parameter list start character (typically an opening parenthesis). As a parameter and parameter separator (typically a comma) are typed, the tooltip is updated to show the next parameter in bold. You can define Signature Help in the context of a language service, or you can define your own file name extension and content type and display Signature Help for just that type, or you can display Signature Help for an existing content type (for example, "text"). This walkthrough shows how to display Signature Help for the "text" content type.  
  
 Signature Help is typically triggered by typing a specific character, for example, "(" (opening parenthesis), and dismissed by typing another character, for example, ")" (closing parenthesis). IntelliSense features that are triggered by typing a character can be implemented by using a command handler for the keystrokes (the <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget> interface) and a handler provider that implements the <xref:Microsoft.VisualStudio.Editor.IVsTextViewCreationListener> interface. To create the Signature Help source, which is the list of signatures that participate in Signature Help, implement the <xref:Microsoft.VisualStudio.Language.Intellisense.ISignatureHelpSource> interface and a source provider that implements the <xref:Microsoft.VisualStudio.Language.Intellisense.ISignatureHelpSourceProvider> interface. The providers are Managed Extensibility Framework (MEF) component parts, and are responsible for exporting the source and controller classes and importing services and brokers, for example, the <xref:Microsoft.VisualStudio.Text.Operations.ITextStructureNavigatorSelectorService>, which lets you navigate in the text buffer, and the <xref:Microsoft.VisualStudio.Language.Intellisense.ISignatureHelpBroker>, which triggers the Signature Help session.  
  
 This walkthrough shows how to implement Signature Help for a hard-coded set of identifiers. In full implementations, the language is responsible for providing that content.  
  
## Prerequisites  
 Starting in Visual Studio 2015, you do not install the Visual Studio SDK from the download center. It is included as an optional feature in Visual Studio setup. You can also install the VS SDK later on. For more information, see [Installing the Visual Studio SDK](../extensibility/installing-the-visual-studio-sdk.md).  
  
## Creating a MEF Project  
  
#### To create a MEF project  
  
1.  Create a C# VSIX project. (In the **New Project** dialog, select **Visual C# / Extensibility**, then **VSIX Project**.) Name the solution `SignatureHelpTest`.  
  
2.  Add an Editor Classifier item template to the project. For more information, see [Creating an Extension with an Editor Item Template](../extensibility/creating-an-extension-with-an-editor-item-template.md).  
  
3.  Delete the existing class files.  
  
4.  Add the following references to the project, and make sure **CopyLocal** is set to `false`:  
  
     Microsoft.VisualStudio.Editor  
  
     Microsoft.VisualStudio.Language.Intellisense  
  
     Microsoft.VisualStudio.OLE.Interop  
  
     Microsoft.VisualStudio.Shell.14.0  
  
     Microsoft.VisualStudio.TextManager.Interop  
  
## Implementing Signature Help Signatures and Parameters  
 The Signature Help source is based on signatures that implement <xref:Microsoft.VisualStudio.Language.Intellisense.ISignature>, each of which contains parameters that implement <xref:Microsoft.VisualStudio.Language.Intellisense.IParameter>. In a full implementation, this information would be obtained from the language documentation, but in this example, the signatures are hard-coded.  
  
#### To implement the Signature Help signatures and parameters  
  
1.  Add a class file and name it `SignatureHelpSource`.  
  
2.  Add the following imports.  
  
     [!CODE [VSSDKSignatureHelpTest#1](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#1)]  
  
3.  Add a class named `TestParameter` that implements <xref:Microsoft.VisualStudio.Language.Intellisense.IParameter>.  
  
     [!CODE [VSSDKSignatureHelpTest#2](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#2)]  
  
4.  Add a constructor that sets all the properties.  
  
     [!CODE [VSSDKSignatureHelpTest#3](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#3)]  
  
5.  Add the properties of <xref:Microsoft.VisualStudio.Language.Intellisense.IParameter>.  
  
     [!CODE [VSSDKSignatureHelpTest#4](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#4)]  
  
6.  Add a class named `TestSignature` that implements <xref:Microsoft.VisualStudio.Language.Intellisense.ISignature>.  
  
     [!CODE [VSSDKSignatureHelpTest#5](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#5)]  
  
7.  Add some private fields.  
  
     [!CODE [VSSDKSignatureHelpTest#6](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#6)]  
  
8.  Add a constructor that sets the fields and subscribes to the <xref:Microsoft.VisualStudio.Text.ITextBuffer.Changed> event.  
  
     [!CODE [VSSDKSignatureHelpTest#7](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#7)]  
  
9. Declare a `CurrentParameterChanged` event. This event is raised when the user fills in one of the parameters in the signature.  
  
     [!CODE [VSSDKSignatureHelpTest#8](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#8)]  
  
10. Implement the <xref:Microsoft.VisualStudio.Language.Intellisense.ISignature.CurrentParameter*> property so that it raises the `CurrentParameterChanged` event when the property value is changed.  
  
     [!CODE [VSSDKSignatureHelpTest#9](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#9)]  
  
11. Add a method that raises the `CurrentParameterChanged` event.  
  
     [!CODE [VSSDKSignatureHelpTest#10](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#10)]  
  
12. Add a method that computes the current parameter by comparing the number of commas in the <xref:Microsoft.VisualStudio.Language.Intellisense.ISignature.ApplicableToSpan*> to the number of commas in the signature.  
  
     [!CODE [VSSDKSignatureHelpTest#11](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#11)]  
  
13. Add an event handler for the <xref:Microsoft.VisualStudio.Text.ITextBuffer.Changed> event that calls the `ComputeCurrentParameter()` method.  
  
     [!CODE [VSSDKSignatureHelpTest#12](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#12)]  
  
14. Implement the <xref:Microsoft.VisualStudio.Language.Intellisense.ISignature.ApplicableToSpan*> property. This property holds an <xref:Microsoft.VisualStudio.Text.ITrackingSpan> that corresponds to the span of text in the buffer to which the signature applies.  
  
     [!CODE [VSSDKSignatureHelpTest#13](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#13)]  
  
15. Implement the other parameters.  
  
     [!CODE [VSSDKSignatureHelpTest#14](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#14)]  
  
## Implementing the Signature Help Source  
 The Signature Help source is the set of signatures for which you provide information.  
  
#### To implement the Signature Help source  
  
1.  Add a class named `TestSignatureHelpSource` that implements <xref:Microsoft.VisualStudio.Language.Intellisense.ISignatureHelpSource>.  
  
     [!CODE [VSSDKSignatureHelpTest#15](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#15)]  
  
2.  Add a reference to the text buffer.  
  
     [!CODE [VSSDKSignatureHelpTest#16](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#16)]  
  
3.  Add a constructor that sets the text buffer and the Signature Help source provider.  
  
     [!CODE [VSSDKSignatureHelpTest#17](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#17)]  
  
4.  Implement the <xref:Microsoft.VisualStudio.Language.Intellisense.ISignatureHelpSource.AugmentSignatureHelpSession*> method. In this example, the signatures are hard-coded, but in a full implementation you would get this information from the language documentation.  
  
     [!CODE [VSSDKSignatureHelpTest#18](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#18)]  
  
5.  The helper method `CreateSignature()` is provided just for illustration.  
  
     [!CODE [VSSDKSignatureHelpTest#19](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#19)]  
  
6.  Implement the <xref:Microsoft.VisualStudio.Language.Intellisense.ISignatureHelpSource.GetBestMatch*> method. In this example, there are just two signatures, each of which has two parameters. Therefore, this method is not required. In a fuller implementation, in which more than one Signature Help source is available, this method is used to decide whether the highest-priority Signature Help source can supply a matching signature. If it cannot, the method returns null and the next-highest-priority source is asked to supply a match.  
  
     [!CODE [VSSDKSignatureHelpTest#20](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#20)]  
  
7.  Implement the Dispose() method:  
  
     [!CODE [VSSDKSignatureHelpTest#21](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#21)]  
  
## Implementing the Signature Help Source Provider  
 The Signature Help source provider is responsible for exporting the Managed Extensibility Framework (MEF) component part and for instantiating the Signature Help source.  
  
#### To implement the Signature Help source provider  
  
1.  Add a class named `TestSignatureHelpSourceProvider` that implements <xref:Microsoft.VisualStudio.Language.Intellisense.ISignatureHelpSourceProvider>, and export it with a <xref:Microsoft.VisualStudio.Utilities.NameAttribute>, a <xref:Microsoft.VisualStudio.Utilities.ContentTypeAttribute> of "text", and an <xref:Microsoft.VisualStudio.Utilities.OrderAttribute> of Before="default".  
  
     [!CODE [VSSDKSignatureHelpTest#22](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#22)]  
  
2.  Implement <xref:Microsoft.VisualStudio.Language.Intellisense.ISignatureHelpSourceProvider.TryCreateSignatureHelpSource*> by instantiating the `TestSignatureHelpSource`.  
  
     [!CODE [VSSDKSignatureHelpTest#23](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#23)]  
  
## Implementing the Command Handler  
 Signature Help is typically triggered by a ( character and dismissed by a ) character. You can handle these keystrokes by implementing a <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget> so that it triggers a Signature Help session when it receives a ( character preceded by a known method name, and dismisses the session when it receives a ) character.  
  
#### To implement the command handler  
  
1.  Add a class named `TestSignatureHelpCommand` that implements <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget>.  
  
     [!CODE [VSSDKSignatureHelpTest#24](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#24)]  
  
2.  Add private fields for the <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView> adapter (which lets you add the command handler to the chain of command handlers), the text view, the Signature Help broker and session, a <xref:Microsoft.VisualStudio.Text.Operations.ITextStructureNavigator>, and the next <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget>.  
  
     [!CODE [VSSDKSignatureHelpTest#25](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#25)]  
  
3.  Add a constructor to initialize these fields and to add the command filter to the chain of command filters.  
  
     [!CODE [VSSDKSignatureHelpTest#26](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#26)]  
  
4.  Implement the <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget.Exec*> method to trigger the Signature Help session when the command filter receives a ( character after one of the known method names, and to dismiss the session when it receives a ) character while the session is still active. In every case, the command is forwarded.  
  
     [!CODE [VSSDKSignatureHelpTest#27](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#27)]  
  
5.  Implement the <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget.QueryStatus*> method so that it always forwards the command.  
  
     [!CODE [VSSDKSignatureHelpTest#28](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#28)]  
  
## Implementing the Signature Help Command Provider  
 You can provide the Signature Help command by implementing the <xref:Microsoft.VisualStudio.Editor.IVsTextViewCreationListener> to instantiate the command handler when the text view is created.  
  
#### To implement the Signature Help command provider  
  
1.  Add a class named `TestSignatureHelpController` that implements <xref:Microsoft.VisualStudio.Editor.IVsTextViewCreationListener> and export it with the <xref:Microsoft.VisualStudio.Utilities.NameAttribute>, <xref:Microsoft.VisualStudio.Utilities.ContentTypeAttribute>, and <xref:Microsoft.VisualStudio.Text.Editor.TextViewRoleAttribute>.  
  
     [!CODE [VSSDKSignatureHelpTest#29](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#29)]  
  
2.  Import the <xref:Microsoft.VisualStudio.Editor.IVsEditorAdaptersFactoryService> (used to get the <xref:Microsoft.VisualStudio.Text.Editor.ITextView>, given the <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView> object), the <xref:Microsoft.VisualStudio.Text.Operations.ITextStructureNavigatorSelectorService> (used to find the current word), and the <xref:Microsoft.VisualStudio.Language.Intellisense.ISignatureHelpBroker> (to trigger the Signature Help session).  
  
     [!CODE [VSSDKSignatureHelpTest#30](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#30)]  
  
3.  Implement the <xref:Microsoft.VisualStudio.Editor.IVsTextViewCreationListener.VsTextViewCreated*> method by instantiating the `TestSignatureCommandHandler`.  
  
     [!CODE [VSSDKSignatureHelpTest#31](../CodeSnippet/VS_Snippets_VSSDK/vssdksignaturehelptest#31)]  
  
## Building and Testing the Code  
 To test this code, build the SignatureHelpTest solution and run it in the experimental instance.  
  
#### To build and test the SignatureHelpTest solution  
  
1.  Build the solution.  
  
2.  When you run this project in the debugger, a second instance of Visual Studio is instantiated.  
  
3.  Create a text file and type some text that includes the word "add" plus an opening parenthesis.  
  
4.  After you type the opening parenthesis, you should see a tooltip that displays a list of the two signatures for the `add()` method.  
  
## See Also  
 [Walkthrough: Linking a Content Type to a File Name Extension](../extensibility/walkthrough--linking-a-content-type-to-a-file-name-extension.md)