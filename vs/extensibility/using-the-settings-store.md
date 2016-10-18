---
title: "Using the Settings Store"
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
  - "Settings Store, using"
ms.assetid: 447ec08a-eca5-40b8-89b0-f98fdf3d39a4
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
# Using the Settings Store
There are two kinds of settings stores:  
  
-   Configuration settings, which are read-only Visual Studio and VSPackage settings. Visual Studio merges settings from all known .pkgdef files into this store.  
  
-   User settings, which are writeable settings such as those that are displayed on pages in the **Options** dialog box, property pages, and certain other dialog boxes. Visual Studio extensions may use these for local storage of small amounts of data.  
  
 This walkthrough shows how to read data from the configuration setting store. See [Writing to the User Settings Store](../extensibility/writing-to-the-user-settings-store.md) for an explanation of how to write to the user settings store.  
  
## Creating the Example Project  
 This section shows how to create a simple extension project with a menu command for demonstration.  
  
1.  Every Visual Studio extension starts with a VSIX deployment project which will contain the extension assets. Create a [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] VSIX project named `SettingsStoreExtension`. You can find the VSIX project template in the **New Project** dialog under **Visual C# / Extensibility**.  
  
2.  Now add a custom command item template named **SettingsStoreCommand**. In the **Add New Item** dialog, go to **Visual C# / Extensibility** and select **Custom Command**. In the **Name** field at the bottom of the window, change the command file name to **SettingsStoreCommand.cs**. For more information about how to create a custom command, see [Creating an Extension with a Menu Command](../extensibility/creating-an-extension-with-a-menu-command.md)  
  
## Using the Configuration Settings Store  
 This section shows how to detect and display configuration settings.  
  
1.  In the SettingsStorageCommand.cs file, add the following using statements:  
  
    ```  
    using System.Collections.Generic;  
    using Microsoft.VisualStudio.Settings;  
    using Microsoft.VisualStudio.Shell.Settings;  
    using System.Windows.Forms;  
    ```  
  
2.  In `MenuItemCallback`, remove the body of the method, and add these lines get the configuration settings store:  
  
    ```  
    SettingsManager settingsManager = new ShellSettingsManager(ServiceProvider);  
    SettingsStore configurationSettingsStore = settingsManager.GetReadOnlySettingsStore(SettingsScope.Configuration);  
    ```  
  
     The <xref:Microsoft.VisualStudio.Shell.Settings.ShellSettingsManager> is a managed helper class over the <xref:Microsoft.VisualStudio.Shell.Interop.IVsSettingsManager> service.  
  
3.  Now find out whether Windows Phone Tools are installed. The code should look like this:  
  
    ```  
    private void MenuItemCallback(object sender, EventArgs e)  
    {  
        SettingsManager settingsManager = new ShellSettingsManager(ServiceProvider);  
        SettingsStore configurationSettingsStore = settingsManager.GetReadOnlySettingsStore(SettingsScope.Configuration);  
        bool arePhoneToolsInstalled = configurationSettingsStore.CollectionExists(@"InstalledProducts\Microsoft Windows Phone Developer Tools");  
        string message = "Microsoft Windows Phone Developer Tools: " + arePhoneToolsInstalled;  
        MessageBox.Show(message);  
    }  
    ```  
  
4.  Test the code. Build the project and start debugging.  
  
5.  In the experimental instance, on the **Tools** menu, click **Invoke SettingsStoreCommand**.  
  
     You should see a message box saying **Microsoft Windows Phone Developer Tools:**  followed by **True** or **False**.  
  
 Visual Studio keeps the settings store in the system registry.  
  
#### To use a registry editor to verify configuration settings  
  
1.  Open Regedit.exe.  
  
2.  Navigate to HKEY_CURRENT_USER\Software\Microsoft\VisualStudio\14.0Exp_Config\InstalledProducts\\.  
  
    > [!NOTE]
    >  Make sure that you are looking at the key that contains \14.0Exp_Config\ and not \14.0_Config\\. When you run the experimental instance of Visual Studio, configuration settings are in the registry hive "14.0Exp_Config".  
  
3.  Expand the \Installed Products\ node. If the message in the previous steps is **Microsoft Windows Phone Developer Tools Installed: True**, then \Installed Products\ should contain a Microsoft Windows Phone Developer Tools node. If the message is **Microsoft Windows Phone Developer Tools Installed: False**, then \Installed Products\ should not contain a Microsoft Windows Phone Developer Tools node.