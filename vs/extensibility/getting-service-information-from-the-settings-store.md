---
title: "Getting Service Information from the Settings Store | hehe"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: 7028d440-d16d-4b08-9b94-eb8cc93b25fc
caps.latest.revision: 4
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
# Getting Service Information from the Settings Store
You can use the settings store to find all available services or to determine whether a particular service is installed. You must know the type of the service class.  
  
### To list the available services  
  
1.  Create a VSIX project named FindServicesExtension and then add a custom command named FindServicesCommand. For more information about how to create a custom command, see [Creating an Extension with a Menu Command](../extensibility/creating-an-extension-with-a-menu-command.md)  
  
2.  In FindServicesCommand.cs, add the following using statements:  
  
    ```vb  
    using System.Collections.Generic;  
    using Microsoft.VisualStudio.Settings;  
    using Microsoft.VisualStudio.Shell.Settings;  
    using System.Windows.Forms;  
    ```  
  
3.  Get the configuration settings store, then find the subcollection named Services. This collection includes all the available services. In the MenuItemCommand method, remove the existing code and replace it with the following:  
  
    ```  
    private void MenuItemCallback(object sender, EventArgs e)  
    {  
        SettingsManager settingsManager = new ShellSettingsManager(ServiceProvider);  
        SettingsStore configurationSettingsStore = settingsManager.GetReadOnlySettingsStore(SettingsScope.Configuration);  
        string message = "Available services:\n";  
        IEnumerable<string> collection = configurationSettingsStore.GetSubCollectionNames("Services");  
        int n = 0;  
        foreach (string service in collection)  
        {  
            message += configurationSettingsStore.GetString("Services\\" + service, "Name", "Unknown") + "\n";  
        }  
  
        MessageBox.Show(message);  
    }  
    ```  
  
4.  Build the project and start debugging. The experimental instance appears.  
  
5.  In the experimental instance, on the **Tools** menu, click **Invoke FindServicesCommand**.  
  
     You should see a message box listing all the services.  
  
     To verify these settings, you can use the registry editor.  
  
## Finding a Specific Service  
 You can also use the <xref:Microsoft.VisualStudio.Settings.SettingsStore.CollectionExists*> method to determine whether a particular service is installed. You must know the type of the service class.  
  
1.  In the MenuItemCallback of the project you created in the previous procedure, search the configuration settings store for the `Services` collection that has the subcollection named by the GUID of the service. In this case we will look for the Help service.  
  
    ```  
    private void MenuItemCallback(object sender, EventArgs e)  
    {  
        SettingsManager settingsManager = new ShellSettingsManager(ServiceProvider);  
        SettingsStore configurationSettingsStore = settingsManager.GetReadOnlySettingsStore(SettingsScope.Configuration);  
        string helpServiceGUID = typeof(SVsHelpService).GUID.ToString("B").ToUpper();  
        bool hasHelpService = configurationSettingsStore.CollectionExists("Services\\" + helpServiceGUID);  
        string message = "Help Service Available: " + hasHelpService;  
  
        MessageBox.Show(message);  
    }  
    ```  
  
2.  Build the project and start debugging.  
  
3.  In the experimental instance, on the **Tools** menu, click **Invoke FindServicesCommand**.  
  
     You should see a message with the text **Help Service Available:**  followed by **True** or **False**. To verify this setting, you can use a registry editor, as shown in the earlier steps.