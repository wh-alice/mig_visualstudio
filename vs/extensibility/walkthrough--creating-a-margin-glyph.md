---
title: "Walkthrough: Creating a Margin Glyph | Microsoft Docs"
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
  - "editors [Visual Studio SDK], new - margin glyph"
ms.assetid: 814185db-24f9-417f-b3b1-7c5aabb42b45
caps.latest.revision: 29
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
# Walkthrough: Creating a Margin Glyph
You can customize the appearance of editor margins by using custom editor extensions. This walkthrough puts a custom glyph on the indicator margin whenever the word "todo" appears in a code comment.  
  
## Prerequisites  
 Starting in Visual Studio 2015, you do not install the Visual Studio SDK from the download center. It is included as an optional feature in Visual Studio setup. You can also install the VS SDK later on. For more information, see [Installing the Visual Studio SDK](../extensibility/installing-the-visual-studio-sdk.md).  
  
## Creating a MEF Project  
  
1.  Create a C# VSIX project. (In the **New Project** dialog, select **Visual C# / Extensibility**, then **VSIX Project**.) Name the solution `TodoGlyphTest`.  
  
2.  Add an Editor Classifier project item. For more information, see [Creating an Extension with an Editor Item Template](../extensibility/creating-an-extension-with-an-editor-item-template.md).  
  
3.  Delete the existing class files.  
  
## Defining the Glyph  
 Define a glyph by implementing the <xref:Microsoft.VisualStudio.Text.Editor.IGlyphFactory> interface.  
  
#### To define the glyph  
  
1.  Add a class file and name it `TodoGlyphFactory`.  
  
2.  Add the following using declarations.  
  
     [!CODE [VSSDKTodoGlyphTest#1](../CodeSnippet/VS_Snippets_VSSDK/vssdktodoglyphtest#1)]  
  
3.  Add a class named `TodoGlyphFactory` that implements <xref:Microsoft.VisualStudio.Text.Editor.IGlyphFactory>.  
  
     [!CODE [VSSDKTodoGlyphTest#2](../CodeSnippet/VS_Snippets_VSSDK/vssdktodoglyphtest#2)]  
  
4.  Add a private field that defines the dimensions of the glyph.  
  
     [!CODE [VSSDKTodoGlyphTest#3](../CodeSnippet/VS_Snippets_VSSDK/vssdktodoglyphtest#3)]  
  
5.  Implement `GenerateGlyph` by defining the glyph user interface (UI) element. `TodoTag` is defined later in this walkthrough.  
  
     [!CODE [VSSDKTodoGlyphTest#4](../CodeSnippet/VS_Snippets_VSSDK/vssdktodoglyphtest#4)]  
  
6.  Add a class named `TodoGlyphFactoryProvider` that implements <xref:Microsoft.VisualStudio.Text.Editor.IGlyphFactoryProvider>. Export this class with a <xref:Microsoft.VisualStudio.Utilities.NameAttribute> of "TodoGlyph", an <xref:Microsoft.VisualStudio.Utilities.OrderAttribute> of After VsTextMarker, a <xref:Microsoft.VisualStudio.Utilities.ContentTypeAttribute> of "code", and a <xref:Microsoft.VisualStudio.Text.Tagging.TagTypeAttribute> of TodoTag.  
  
     [!CODE [VSSDKTodoGlyphTest#5](../CodeSnippet/VS_Snippets_VSSDK/vssdktodoglyphtest#5)]  
  
7.  Implement the <xref:Microsoft.VisualStudio.Text.Editor.IGlyphFactoryProvider.GetGlyphFactory*> method by instantiating the `TodoGlyphFactory`.  
  
     [!CODE [VSSDKTodoGlyphTest#6](../CodeSnippet/VS_Snippets_VSSDK/vssdktodoglyphtest#6)]  
  
## Defining a Todo Tag and Tagger  
 Define the relationship between the UI element that you defined in the previous steps and the indicator margin by creating a tag type and tagger, and exporting it by using a tagger provider.  
  
#### To define a todo tag and tagger  
  
1.  Add a new class file to the project and name it `TodoTagger`.  
  
2.  Add the following imports.  
  
     [!CODE [VSSDKTodoGlyphTest#7](../CodeSnippet/VS_Snippets_VSSDK/vssdktodoglyphtest#7)]  
  
3.  Add a class named `TodoTag`.  
  
     [!CODE [VSSDKTodoGlyphTest#8](../CodeSnippet/VS_Snippets_VSSDK/vssdktodoglyphtest#8)]  
  
4.  Modify the class named `TodoTagger` that implements <xref:Microsoft.VisualStudio.Text.Tagging.ITagger`1> of type `TodoTag`.  
  
     [!CODE [VSSDKTodoGlyphTest#9](../CodeSnippet/VS_Snippets_VSSDK/vssdktodoglyphtest#9)]  
  
5.  To the `TodoTagger` class, add private fields for an <xref:Microsoft.VisualStudio.Text.Classification.IClassifier> and for the text to find in the classification spans.  
  
     [!CODE [VSSDKTodoGlyphTest#10](../CodeSnippet/VS_Snippets_VSSDK/vssdktodoglyphtest#10)]  
  
6.  Add a constructor that sets the classifier.  
  
     [!CODE [VSSDKTodoGlyphTest#11](../CodeSnippet/VS_Snippets_VSSDK/vssdktodoglyphtest#11)]  
  
7.  Implement the <xref:Microsoft.VisualStudio.Text.Tagging.ITagger`1.GetTags*> method by finding all the classification spans whose names include the word "comment" and whose text includes the search text. Whenever the search text is found, yield back a new <xref:Microsoft.VisualStudio.Text.Tagging.TagSpan`1> of type `TodoTag`.  
  
     [!CODE [VSSDKTodoGlyphTest#12](../CodeSnippet/VS_Snippets_VSSDK/vssdktodoglyphtest#12)]  
  
8.  Declare a `TagsChanged` event.  
  
     [!CODE [VSSDKTodoGlyphTest#13](../CodeSnippet/VS_Snippets_VSSDK/vssdktodoglyphtest#13)]  
  
9. Add a class named `TodoTaggerProvider` that implements <xref:Microsoft.VisualStudio.Text.Tagging.ITaggerProvider>, and export it with a <xref:Microsoft.VisualStudio.Utilities.ContentTypeAttribute> of "code" and a <xref:Microsoft.VisualStudio.Text.Tagging.TagTypeAttribute> of TodoTag.  
  
     [!CODE [VSSDKTodoGlyphTest#14](../CodeSnippet/VS_Snippets_VSSDK/vssdktodoglyphtest#14)]  
  
10. Import the <xref:Microsoft.VisualStudio.Text.Classification.IClassifierAggregatorService>.  
  
     [!CODE [VSSDKTodoGlyphTest#15](../CodeSnippet/VS_Snippets_VSSDK/vssdktodoglyphtest#15)]  
  
11. Implement the <xref:Microsoft.VisualStudio.Text.Tagging.ITaggerProvider.CreateTagger*> method by instantiating the `TodoTagger`.  
  
     [!CODE [VSSDKTodoGlyphTest#16](../CodeSnippet/VS_Snippets_VSSDK/vssdktodoglyphtest#16)]  
  
## Building and Testing the Code  
 To test this code, build the TodoGlyphTest solution and run it in the experimental instance.  
  
#### To build and test the TodoGlyphTest solution  
  
1.  Build the solution.  
  
2.  Run the project by pressing F5. A second instance of Visual Studio is instantiated.  
  
3.  Make sure that the indicator margin is showing. (On the **Tools** menu, click **Options**. On the **Text Editor** page, make sure that **Indicator margin** is selected.)  
  
4.  Open a code file that has comments. Add the word "todo" to one of the comment sections.  
  
5.  A light blue circle that has a dark blue outline should appear in the indicator margin to the left of the code window.