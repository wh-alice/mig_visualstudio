---
title: "How to: Use XML Snippets | testtitle"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-general"
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 3a27375b-81cc-48f6-a884-e1cb8c4f78f5
caps.latest.revision: 2
ms.author: "kempb"
manager: "ghogen"
translation.priority.ht: 
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
# How to: Use XML Snippets
You can invoke XML snippets by using the following two commands on the XML Editor shortcut menu. The **Insert Snippet** command inserts the XML snippet at the cursor position. The **Surround With** command wraps the XML snippet around the selected text. Each XML snippet has designated snippet types. The snippet types determine whether the snippet is available with the **Insert Snippet** command, the **Surround With** command, or both.  
  
 After the XML snippet has been added to the editor, any editable fields in the snippet are highlighted in yellow, and the cursor is positioned on the first editable field.  
  
## Insert Snippet  
 The following procedures describe how to access the **Insert Snippet** command.  
  
> [!NOTE]
>  The **Insert Snippet** command is also available through the keyboard shortcut (CTRL+K, then CTRL+X).  
  
#### To insert snippets from the shortcut menu  
  
1.  Position the cursor where you want to insert the XML snippet.  
  
2.  Right-click and select **Insert Snippet**.  
  
     A list of available XML snippets is displayed.  
  
3.  Select a snippet from the list using the mouse, or by typing the name of the snippet and pressing TAB or ENTER.  
  
#### To insert snippets using the IntelliSense menu  
  
1.  Position the cursor where you want to insert the XML snippet.  
  
2.  From the **Edit** menu, point to **IntelliSense**, and then select **Insert Snippet**.  
  
     A list of available XML snippets is displayed.  
  
3.  Select a snippet from the list using the mouse or by typing the name of the snippet and pressing TAB or ENTER.  
  
#### To insert snippets through the IntelliSense Complete Word list  
  
1.  Position the cursor where you want to insert the XML snippet.  
  
2.  Begin typing the XML snippet that you want to add to your file. If automatic completion is turned on, the IntelliSense complete word list is displayed. If it does not appear, press CTRL+SPACEBAR to activate it.  
  
3.  Select the XML snippet from the complete word list.  
  
4.  Press TAB, TAB to invoke the XML snippet.  
  
> [!NOTE]
>  There may be cases when the XML snippet does not get invoked. For example, if you try to insert an `xs:complexType` element inside an `xs:element` node, the editor does not generate an XML snippet. When an `xs:complexType` element is used inside an `xs:element` node, there are no required attributes or subelements, so the editor does not have any data to insert.  
  
#### To insert snippets using the shortcut name  
  
1.  Position the cursor where you want to insert the XML snippet.  
  
2.  Type `<` in the editor pane.  
  
3.  Press ESC to close the IntelliSense complete word list.  
  
4.  Type the shortcut name of the snippet, and press TAB to invoke the XML snippet.  
  
## Surround With  
 The following procedures describe how to access the **Surround With** command.  
  
> [!NOTE]
>  The **Surround With** command is also available through the keyboard shortcut (CTRL+K, then CTRL+S).  
  
#### To use surround with from the context menu  
  
1.  Select the text to surround in the XML Editor.  
  
2.  Right-click and select **Surround With**.  
  
     A list of available surrounds with XML snippets is displayed.  
  
3.  Select a snippet from the list using the mouse, or by typing the name of the snippet and pressing TAB or ENTER.  
  
#### To use surround with from the Intellisense menu  
  
1.  Select the text to surround in the XML Editor.  
  
2.  From the **Edit** menu, point to **IntelliSense**, and then select **Surround With**.  
  
     A list of available surrounds with XML snippets is displayed.  
  
3.  Select a snippet from the list using the mouse, or by typing the name of the snippet and pressing TAB or ENTER.  
  
## Using XML Snippets  
 Once you choose an XML snippet, the text of the code snippet is inserted automatically at the cursor position. Any editable fields in the snippet are highlighted, and the first editable field is selected automatically. The currently selected field is boxed.  
  
 When a field is selected, you can type a new value for the field. Pressing TAB cycles through the editable fields of the snippet; pressing SHIFT+TAB cycles through them in reverse order. Clicking a field places the cursor in the field, and double-clicking a field selects it. When a field is highlighted, a ToolTip might be displayed, offering a description of the field.  
  
 Only the first instance of a given field is editable. When that field is highlighted, the other instances of that field are outlined. When you change the value of an editable field, that field is changed everywhere it is used in the snippet.  
  
 Pressing ENTER or ESC cancels field editing and returns the editor to normal.  
  
 The default colors for editable code snippet fields can be changed by modifying the Code Snippet Field setting in the **Fonts and Colors** pane of the **Option**s dialog box. For more information, see [How to: Change Fonts and Colors in the Editor](../reference/how-to--change-fonts-and-colors-in-the-editor.md).  
  
## See Also  
 [XML Snippets](../reference/xml-snippets.md)   
 [How to: Generate an XML Snippet From an XML Schema](../reference/how-to--generate-an-xml-snippet-from-an-xml-schema.md)   
 [How to: Create XML Snippets](../reference/how-to--create-xml-snippets.md)