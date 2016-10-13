---
title: "Options Dialog Box (Visual Studio)"
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
  - "vs.toolsoptionspages"
helpviewer_keywords: 
  - "Tools Options settings"
  - "Options dialog box"
  - "Options dialog box, development environment"
  - "tools [Visual Studio], customizing"
ms.assetid: 02b09877-1df1-4531-a0d1-a4ca17c7f857
caps.latest.revision: 19
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
# Options Dialog Box (Visual Studio)
The **Options** dialog box enables you to configure the integrated development environment (IDE) to your needs. For example, you can establish a default save location for your projects, alter the default appearance and behavior of windows, and create shortcuts for commonly used commands. There are also options specific to your development language and platform. You can access **Options** from the **Tools** menu.  
  
> [!NOTE]
>  The options available in dialog boxes, and the names and locations of menu commands you see, might differ from what is described in Help depending on your active settings or edition. To change your settings, choose **Import and Export Settings** on the **Tools** menu. For more information, see [Customizing Development Settings in Visual Studio](assetId:///22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
## Layout of the Options dialog box  
 The **Options** dialog box is divided into two parts: a navigation pane on the left and a display area on the right. The tree control in the navigation pane includes folder nodes, such as Environment, Text Editor, Projects and Solutions, and Source Control. Expand any folder node to list the pages of options that it contains. When you select the node for a particular page, its options appear in the display area.  
  
 Options for an IDE feature do not appear in the navigation pane until the feature is loaded into memory. Therefore, the same options might not be displayed as you begin a new session that were displayed as you ended the last. When you create a project or run a command that uses a particular application, nodes for relevant options are added to the Options dialog box. These added options will then remain available as long as the IDE feature remains in memory.  
  
> [!NOTE]
>  Some settings collections scope the number of pages that appear in the navigation pane of the Options dialog box. You can choose to view all possible pages by selecting **Show all settings**.  
  
## How options are applied  
 Clicking OK in the **Options** dialog box saves all settings on all pages. Clicking Cancel on any page cancels all change requests, including any just made on other **Options** pages. Some changes to option settings, such as those made on [Fonts and Colors, Environment, Options Dialog Box](../reference/fonts-and-colors--environment--options-dialog-box.md), will only take effect after you close and reopen Visual Studio.  
  
### Show all settings  
 Selecting or unselecting **Show all settings** applies all changes you have made in the **Options** dialog box, even though you have not yet clicked **OK**.  
  
## See Also  
 [Customizing the Editor](../ide/customizing-the-editor.md)