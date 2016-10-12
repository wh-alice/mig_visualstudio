---
title: "Multiple DSLs in One Solution"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-tfs-dev14"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
ms.assetid: 7e668620-6217-4e87-aea7-e9036776c8e4
caps.latest.revision: 3
ms.author: "awills"
manager: "kamrani"
---
# Multiple DSLs in One Solution
You can package several DSLs as part of a single solution so that they are installed together.  
  
 You can use several techniques to integrate multiple DSLs. For more information, see [Integrating Models by using Visual Studio Modelbus](../VS_IDE/integrating-models-by-using-visual-studio-modelbus.md) and [How to: Add a Drag-and-Drop Handler](../VS_IDE/how-to--add-a-drag-and-drop-handler.md) and [Customizing Copy Behavior](../VS_IDE/customizing-copy-behavior.md).  
  
### To build more than one DSL in the same solution  
  
1.  Create two or more DSL solutions and a VSIX project, and add all the projects to a single solution.  
  
    -   To create a new VSIX project: In the **New Project** dialog, select **Visual C#**, **Extensibility**, **VSIX Project**.  
  
    -   Create two or more DSL solutions in the VSIX solution directory.  
  
         For each DSL, open a new instance of Visual Studio. Create the new DSL, and specify the same solution folder as the VSIX solution.  
  
         Make sure that you create each DSL with a different filename extension.  
  
    -   Change the names of the **Dsl** and **DslPackage** projects so that they are all different. For example: `Dsl1`, `DslPackage1`, `Dsl2`, `DslPackage2`.  
  
    -   In each **DslPackage\*\source.extension.tt**, update this line to the correct Dsl project name:  
  
         `string dslProjectName = "Dsl2";`  
  
    -   In the VSIX solution, add the Dsl* and DslPackage\* projects.  
  
         You might want to place each pair in its own solution folder.  
  
2.  Combine the VSIX manifests of the DSLs:  
  
    1.  Open *YourVsixProject***\source.extension.manifest**.  
  
    2.  For each DSL, choose **Add Content** and add:  
  
        -   `Dsl*` project as a **MEF Component**  
  
        -   `DslPackage*` project as a **MEF Component**  
  
        -   `DslPackage*` project as a **VS Package**  
  
3.  Build the solution.  
  
 The resulting VSIX will install both DSLs. You can test them by using F5, or deploy *YourVsixProject***\bin\Debug\\\*.vsix**.  
  
## See Also  
 [Integrating Models by using Visual Studio Modelbus](../VS_IDE/integrating-models-by-using-visual-studio-modelbus.md)   
 [How to: Add a Drag-and-Drop Handler](../VS_IDE/how-to--add-a-drag-and-drop-handler.md)   
 [Customizing Copy Behavior](../VS_IDE/customizing-copy-behavior.md)