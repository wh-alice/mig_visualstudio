---
title: "Commands, Menus, and Toolbars"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "menus [Visual Studio SDK], commands"
  - "commands [Visual Studio]"
  - "toolbars [Visual Studio], commands"
ms.assetid: 07b4ed90-dbbd-40df-b6c9-8395fd6f2ab6
caps.latest.revision: 60
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
# Commands, Menus, and Toolbars
Menus and toolbars are the way users access commands in your VSPackage. Commands are functions that accomplish tasks, such as printing a document, refreshing a view, or creating a new file. Menus and toolbars are convenient graphical ways to present your commands to users. Typically, related commands are clustered together on the same menu or toolbar.  
  
-   Menus typically are displayed as one-word strings clustered in a row at the top of the integrated development environment (IDE) or a tool window. Menus also can be displayed as the result of a right-click event, and are referred to as shortcut menus in that context. When clicked, menus expand to display one or more commands. Commands, when clicked, can carry out tasks or launch submenus that contain additional commands. Some well-known menu names are File, Edit, View, and Window. For more information, see [Extending Menus and Commands](../extensibility/extending-menus-and-commands.md).  
  
-   Toolbars typically are rows of buttons and other controls, such as combo boxes, list boxes, text boxes, and menu controllers. All toolbar controls are associated with commands. When you click a toolbar button, its associated command is activated. Toolbar buttons usually have icons that suggest the underlying commands, such as a printer for a Print command. In a drop-down list control, each item in the list is associated with a different command. A menu controller is a hybrid in which one side of the control is a toolbar button and the other side is a down arrow that displays additional commands when clicked. For more information, see [Adding a Menu Controller to a Toolbar](../extensibility/adding-a-menu-controller-to-a-toolbar.md).  
  
-   When you create a command, you also must create an event handler for it. The event handler determines when the command is visible or enabled, allows you to modify its text, and ensures that the command responds appropriately ("routes") when activated. In most instances, the IDE handles commands using the <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget> interface. Commands in [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] route in a hierarchical manner, starting with the innermost command context, based on the local selection, and proceeding to the outermost context, based on the global selection. Commands added to the main menu are immediately available for scripting. For more information, see [MenuCommands Vs. OleMenuCommands](../misc/menucommands-vs.-olemenucommands.md) and [Selection Context Objects](../extensibility/selection-context-objects.md).  
  
 To define new menus and toolbars, you must describe them in an Visual Studio Command Table (.vsct) file. The Visual Studio Package Template creates this file for you, along with the necessary elements to support whatever commands, toolbars, and editors you selected in the template. Alternatively, you can write your own .vsct file, using the xml schema described here: [VSCT XML Schema Reference](../extensibility/vsct-xml-schema-reference.md).  
  
 For more information about working with .vsct files, see [Visual Studio Command Table (.Vsct) Files](../extensibility/visual-studio-command-table--.vsct--files.md).  
  
 The topics in this section explain how commands, menus, and toolbars work in VSPackages.  
  
## In This Section  
 [How VSPackages Add User Interface Elements](../extensibility/how-vspackages-add-user-interface-elements.md)  
 An in-depth description of the Command Table Format specification.  
  
 [Visual Studio Command Table (.Vsct) Files](../extensibility/visual-studio-command-table--.vsct--files.md)  
 Describes an XML-based syntax and compiler for command tables.  
  
 [Default Command, Group, and Toolbar Placement](../extensibility/default-command--group--and-toolbar-placement.md)  
 Describes predefined commands, groups, menus, and toolbars.  
  
 [IDE-Defined Commands, Menus, and Groups](../extensibility/ide-defined-commands--menus--and-groups.md)  
 Specifies the predefined menus, commands, and command groups available for use by the [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] IDE.  
  
 [Command Design](../extensibility/command-design.md)  
 Explains how to design commands.  
  
 [Optimizing Menu and Toolbar Commands](../extensibility/optimizing-menu-and-toolbar-commands.md)  
 Gives guidelines for commands.  
  
 [Making Commands Available](../extensibility/making-commands-available.md)  
 Explains how to make commands available to Visual Studio.  
  
 [Commands and Menus That Use Interop Assemblies](../extensibility/commands-and-menus-that-use-interop-assemblies.md)  
 Explains how to implement commands that use interop assemblies.  
  
## Related Sections  
 [Command Routing in VSPackages](../extensibility/command-routing-in-vspackages.md)  
 Explains command routing in VSPackages.