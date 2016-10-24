---
title: "Getting Started with the VSIX Project Template | Microsoft Docs"
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
  - "Visual Studio SDK, VSIX project template"
ms.assetid: 89fac33e-9380-4723-9b45-048a6e16f0ed
caps.latest.revision: 25
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
# Getting Started with the VSIX Project Template
You can use the VSIX Project template to create an extension or to package an existing extension for deployment. The VSIX Project template has both Visual Basic and Visual C# versions, and is installed as part of the Visual Studio SDK.  
  
 The VSIX Project template just consists of a source.extension.vsixmanifest file, which contains information about the extension and the assets it ships.  
  
 To find the VSIX project template, you must install the Visual Studio SDK. For more information, see [Visual Studio SDK](../extensibility/visual-studio-sdk.md).  
  
## Deploying a Custom Project Template using the VSIX Project Template  
 The following steps show how to use the VSIX project to package a project template that you can share with other developers or upload to the Visual Studio Gallery.  
  
1.  Create a project template.  
  
    1.  Open the project from which to create a template. This project can be of any project type.  
  
    2.  On the **File** menu, click **Export Template**. Complete the steps of the wizard.  
  
         A .zip file is created in %USERPROFILE%\My Documents\Visual Studio *\<version>*\My Exported Templates\\.  
  
2.  Create an empty VSIX project.  
  
     On the **File** menu, click **New** and then click **Project**. Select either **Visual Basic** or **Visual C#**. Under the selected node, select **Extensibility**, and then select **VSIX Project**.  
  
3.  Add the .zip file to the project. Set its **Copy to Output Directory** property to `Copy Always`.  
  
4.  In the **Solution Explorer**, double-click the `source.extension.vsixmanifest` file to open it in the **VSIX Manifest Designer**, and then make the following changes:  
  
    -   Set the **Product Name** field to **My Project Template**.  
  
    -   Set the **Product ID** field to **MyProjectTemplate - 1**.  
  
    -   Set the **Author** field to **Fabrikam**.  
  
    -   Set the **Description** field to **My project template**.  
  
    -   In the **Assets** section, add a **Microsoft.VisualStudio.ProjectTemplate** type and set its path to the name of the .zip file.  
  
5.  Save and close the source.extension.vsixmanifest file.  
  
6.  Build the project.  
  
7.  In the output directory, double-click the .vsix file.  
  
8.  A **VSIX Installer** message box appears. Follow the instructions to install the extension.  
  
9. Close Visual Studio and then re-open it.  
  
10. Select **Extensions and Updates** (on the **Tools** menu) and select the **Templates** category. One of the available extensions should be **My Project Template**.  
  
11. The new project template appears in the **New Project** dialog in the same place as the original project template. For example, if you created a template named **VB Console** from a Visual Basic console application, **VB Console** appears in the same pane as the Visual Basic **Console Application** template.  
  
#### To Specify the Location of the Template in the New Project Dialog Box  
  
1.  Template folders are located in the *Visual Studio Installation Path*\Common7\IDE\ProjectTemplates and *Visual Studio Installation Path*\Common7\IDE\ItemTemplates directories. The names of the top level sections in the New Project dialog do not exactly match the names of the template folders. Where they differ, use the name of the template folder.  
  
     Change the .vsix file extension to .zip, and then open the file.  
  
2.  Create a new folder with the same name as the section of the New Project dialog the template should appear in.  
  
3.  If the template is to appear in a subsection, create a subfolder of the same name.  
  
4.  Move the template .zip file into the new folder.  
  
5.  Change the .zip extension to .vsix.  
  
6.  Open the VSIX manifest.  
  
7.  In the VSIX manifest, update the **Asset** path of the template so that it points to the root of the directory tree that contains the template file. For example, if the template is in \CSharp\Windows, the reference should point to \CSharp.