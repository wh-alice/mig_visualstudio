---
title: "Using the Toolbox"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-general"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "vs.chooseitems"
  - "vs.toolboxpages.activexcontrols"
  - "VS.CHOOSEITEMS.windowsuixamlcomponents"
  - "VS.chooseitems.silverlightcomponents"
  - "VC.EDITORS.RIBBON"
  - "vs.customizetoolbox"
  - "VS.chooseitems.System.Workflow_Components"
  - "vs.chooseitems.frameworkcomponents"
  - "VS.ToolboxPages..NET_Framework_Components"
  - "VS.chooseitems.Microsoft.VisualStudio.Toolbox.VsToolboxPage"
  - "vs.chooseitems.comcomponents"
  - "vs.toolboxpages.NGWS_components"
helpviewer_keywords: 
  - "toolbox, adding items"
  - "Visual Studio, toolbox"
  - "toolbox, tabs"
  - "toolbox"
ms.assetid: 82e7cb43-4d0b-4e17-b7b0-43f96c22c3c2
caps.latest.revision: 20
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
# Using the Toolbox
You can use the toolbox to add controls and other items to your project. You can drag and drop different controls onto the surface of the designer you are using, and resize and position the controls.  
  
 The toolbox appears in conjunction with designer views, such as the designer view of a XAML file. The toolbox displays only those controls that can be used in the current designer.  
  
 The .NET Framework version that your project targets also affects the set of controls visible in the toolbox. By default, [!INCLUDE[vs_dev12](../VS_IDE/includes/vs_dev12_md.md)] projects target the .NET Framework 4.5.1. You can set your project to target a different version of the .NET Framework by selecting the project node in **Solution Explorer**, and then browsing to **Properties/Application/Target Framework**.  
  
## Managing the Toolbox and its Controls  
 By default the toolbox is collapsed along the left side of the Visual Studio IDE, and appears when the cursor is moved over it. You can pin the toolbox (by clicking the **Pin** icon on the toolbox toolbar) so that it remains open when you move the cursor. You can also undock the toolbox window and drag it anywhere on your screen. You can dock, undock, and hide the toolbox by right-clicking the toolbox toolbar and selecting one of the options.  
  
 You can rearrange the items in a toolbox tab or add custom tabs and items by using the following commands on the context menu:  
  
-   **Rename item** - Renames the selected item.  
  
-   **Show All** - Shows all possible controls (not just the ones that apply to the current designer).  
  
-   **List View** - Shows the controls in a vertical list. If unchecked, the controls appear horizontally.  
  
-   **Choose Items** - Opens the **Choose Toolbox Items** dialog box so that you can specify the items that appear in the **Toolbox**. You can show or hide an item by selecting or clearing its check box.  
  
-   **Sort items alphabetically** - Sorts the items by name.  
  
-   **Reset Toolbar** - Restores the default toolbox settings and items.  
  
-   **Add Tab** - Adds a new toolbox tab.  
  
-   **Move Up** - Moves the selected item up.  
  
-   **Move Down** - Moves the selected item down.  
  
## Creating and Distributing Custom Toolbox Controls  
 You can create a custom toolbox control in either Visual Basic or Visual C#, and you can start with a project template that's based on [Windows Presentation Foundation](../Topic/Creating%20a%20WPF%20Toolbox%20Control.md) or [Windows Forms](../VS_not_in_toc/how-to--create-a-toolbox-control-that-uses-windows-forms.md). You can then distribute your control to your teammates or publish it on the web by using the [Toolbox Controls Installer](http://download.microsoft.com/download/8/3/6/836657BD-9CCB-4ED4-B9D2-FB769473B284/TCI_whitepaper.docx).