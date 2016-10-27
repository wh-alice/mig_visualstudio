---
title: "Error List Window"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-general"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "VS.ErrorList"
helpviewer_keywords: 
  - "Task List"
  - "build errors"
  - "Error List window"
  - "errors [Visual Studio], Error List window"
ms.assetid: b7f6d45a-733b-4ad8-bc2f-737a37509e56
caps.latest.revision: 32
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
# Error List Window
> [!NOTE]
>  The Error List displays information about a specific error message. You can copy the error number or error string text from the Output window. To display the Output window, press Ctrl+Alt+O. See [Output Window](../../ide/reference/output-window.md).  
  
 You can develop apps faster by using the **Error List** window. For example, you can perform the following tasks:  
  
-   Display the errors, warnings, and messages produced while you write code.  
  
-   Find syntax errors noted by IntelliSense.  
  
-   Find deployment errors, certain Static Analysis errors, and errors detected while applying Enterprise Template policies.  
  
-   Double-click any error message entry to open the file where the problem occurs, and move to the error location.  
  
-   Filter which entries are displayed, and which columns of information appear for each entry.  
  
-   Search for specific terms and scope the search to just the current project or document.  
  
 To display the **Error List**, click **View / Error List**, or **CTRL+\\+E**.  
  
 You can choose the **Errors**, **Warnings**, and **Messages** tabs to see different levels of information.  
  
 To sort the list, click any column header. To sort again by an additional column, hold down the SHIFT key and click another column header. To select which columns are displayed and which are hidden, choose **Show Columns** from the shortcut menu. To change the order in which columns are displayed, drag any column header to the left or right.  
  
> [!NOTE]
>  The dialog boxes and menu commands you see might differ from those described here, depending on your active settings or edition. To change your settings, click **Tools / Import and Export Settings**. For more information, see [Customizing Development Settings in Visual Studio](http://msdn.microsoft.com/en-us/22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
## Error List Filters  
 There are two types of filter in two dropdown boxes, one on the right side of the toolbar and one to the left of the toolbar. The dropdown list on the left side of the toolbar specifies the set of code files to use (**Entire Solution**, **Open Documents**, **Current Project**, **Current Document**).  
  
 You can restrict the scope of the search to analyze and act on groups of errors. For example, you might want to focus on core errors that are preventing a project from compiling. The scoping options include:  
  
1.  **Open Documents**: Show errors, warnings, and messages for the open documents.  
  
2.  **Current Project**: Show errors, warnings, and messages from the project of the currently selected document in the **Editor** or the selected project in **Solution Explorer**.  
  
    > [!NOTE]
    >  The filtered list of errors, warnings, and messages will change if the project of the currently selected document is different from the project selected in **Solution Explorer**.  
  
3.  **Current Document**: Show errors, warnings, and messages for the currently selected document in the **Editor** or **Solution Explorer**.  
  
 If a filter is currently applied to the search result, the name of the filter appears in the **Error List** title bar. The **Errors**, **Warnings**, and **Messages** buttons then display the number of filtered items being shown along with the total number of items; for example, the buttons show x of y Errors. If no filter is applied, the title bar says only “Error List”.  
  
 The list on the right side of the toolbar specifies whether to show errors from the build (errors resulting from a build operation) or from IntelliSense (errors detected before running a build), or from both.  
  
## Search  
 Use the **Search Error List** text box on the right side of the **Error List** toolbar to find specific errors in the error list. You can search on any visible column in the error list, and search results are always sorted based on the column that has sort priority instead of on the query or the filter applied. If you choose the **Esc** key while the focus is in the **Error List**, you can clear the search term and filtered search results. You can also click the **X** on the right side of the text box to clear it.  
  
## Save  
 You can copy the error list and save it to a file. Select the errors you want to copy and right-click the selection, then on the context menu select **Copy**. You can then paste the errors into a file. If you paste the errors to an Excel spreadsheet, the fields appear as different columns.  
  
## UI Element List  
 Severity  
 Displays the different types of **Error List** entry (**Error**, **Message**, **Warning**, **Warning (active)**, **Warning (inactive)**.  
  
 Code  
 Displays the error code.  
  
 Description  
 Displays the text of the entry.  
  
 Project  
 Displays the name of the current project.  
  
 File  
 Displays the file name.  
  
 Line  
 Displays the line where the problem occurs.