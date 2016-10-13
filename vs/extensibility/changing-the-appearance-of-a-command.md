---
title: "Changing the Appearance of a Command"
ms.custom: na
ms.date: "10/13/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "commands, changing appearance"
  - "menu commands, changing appearance"
  - "menus, changing command appearance"
ms.assetid: da2474fa-f92d-4e9e-b8bf-67c61bf249c2
caps.latest.revision: 23
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
# Changing the Appearance of a Command
You can provide feedback to your user by changing the appearance of a command. For example, you may want a command to look different when it is unavailable. You can make commands available or unavailable, hide or show them, or check or uncheck them on the menu.  
  
 To change the appearance of a command, perform one of these actions:  
  
-   Specify the appropriate flags in the command definition in the command table file.  
  
-   Use the \<xref:Microsoft.VisualStudio.Shell.OleMenuCommandService> service.  
  
-   Implement the \<xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget> interface and modify the raw command objects.  
  
 The following steps show how to find and update the appearance of a command by using the Managed Package Framework (MPF).  
  
### To change the appearance of a menu command  
  
1.  Follow the instructions in [Changing the Text of a Menu Command](../extensibility/changing-the-text-of-a-menu-command.md) to create a menu item named `New Text`.  
  
2.  In the ChangeMenuText.cs file, add the following using statement:  
  
    ```c#  
    using System.Security.Permissions;  
    ```  
  
3.  In the ChangeMenuTextPackageGuids.cs file, add the following line:  
  
    ```c#  
    public const string guidChangeMenuTextPackageCmdSet= "00000000-0000-0000-0000-00000000";  // get the GUID from the .vsct file  
    ```  
  
4.  In the ChangeMenuText.cs file, replace the code in the ShowMessageBox method with the following:  
  
    ```c#  
    private void ShowMessageBox(object sender, EventArgs e)  
    {  
        var command = sender as OleMenuCommand;  
        if (command.Text == "New Text")  
            ChangeMyCommand(command.CommandID.ID, false);}  
    }  
    ```  
  
5.  Obtain the command that you want to update from the \<xref:Microsoft.VisualStudio.Shell.OleMenuCommandService> object and then set the appropriate properties on the command object. For example, the following method makes the specified command from a VSPackage command set available or unavailable. The following code makes the menu item named `New Text` unavailable after it has been clicked.  
  
    ```c#  
    public bool ChangeMyCommand(int cmdID, bool enableCmd)  
    {  
        bool cmdUpdated = false;  
        var mcs = this.ServiceProvider.GetService(typeof(IMenuCommandService))  
            as OleMenuCommandService;  
        var newCmdID = new CommandID(new Guid(ChangeMenuTextPackageGuids.guidChangeMenuTextPackageCmdSet), cmdID);  
        MenuCommand mc = mcs.FindCommand(newCmdID);  
        if (mc != null)  
        {  
            mc.Enabled = enableCmd;  
            cmdUpdated = true;  
        }  
        return cmdUpdated;    }  
    }  
    ```  
  
6.  Build the project and start debugging. The experimental instance of Visual Studio should appear.  
  
7.  On the **Tools** menu, click the **Invoke ChangeMenuText** command. At this point the command name is **Invoke ChangeMenuText**, so the command handler doesn’t call ChangeMyCommand().  
  
8.  On the **Tools** menu you should now see **New Text**. Click **New Text**. The command should now be grayed out.  
  
## See Also  
 [Commands, Menus, and Toolbars](../extensibility/commands--menus--and-toolbars.md)   
 [How VSPackages Add User Interface Elements](../extensibility/how-vspackages-add-user-interface-elements.md)   
 [Extending Menus and Commands](../extensibility/extending-menus-and-commands.md)   
 [Visual Studio Command Table (.Vsct) Files](../extensibility/visual-studio-command-table--.vsct--files.md)