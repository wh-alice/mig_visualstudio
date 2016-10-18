---
title: "Extending the Output Window"
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
  - "Output window, about Output window"
ms.assetid: b02fa88c-f92a-4ff6-ba5f-2eb4d48a643a
caps.latest.revision: 13
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
# Extending the Output Window
The **Output** window is a set of read/write text panes. Visual Studio has these built-in panes: **Build**, in which projects communicate messages about builds, and **General**, in which [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] communicates messages about the IDE. Projects get a reference to the **Build** pane automatically through the <xref:Microsoft.VisualStudio.Shell.Interop.IVsBuildableProjectCfg> interface methods, and Visual Studio offers direct access to the **General** pane through the <xref:Microsoft.VisualStudio.Shell.Interop.SVsGeneralOutputWindowPane> service. In addition to the built-in panes, you can create and manage your own custom panes.  
  
 You can control the **Output** window directly through the <xref:Microsoft.VisualStudio.Shell.Interop.IVsOutputWindow> and <xref:Microsoft.VisualStudio.Shell.Interop.IVsOutputWindowPane> interfaces. The <xref:Microsoft.VisualStudio.Shell.Interop.IVsOutputWindow> interface, which is offered by the <xref:Microsoft.VisualStudio.Shell.Interop.SVsOutputWindow> service, defines methods for creating, retrieving, and destroying **Output** window panes. The <xref:Microsoft.VisualStudio.Shell.Interop.IVsOutputWindow> interface defines methods for showing panes, hiding panes, and manipulating their text. An alternative way of controlling the **Output** window is through the <xref:EnvDTE.OutputWindow> and <xref:EnvDTE.OutputWindowPane> objects in the Visual Studio Automation object model. These objects encapsulate nearly all of the functionality of the <xref:Microsoft.VisualStudio.Shell.Interop.IVsOutputWindow> and <xref:Microsoft.VisualStudio.Shell.Interop.IVsOutputWindowPane> interfaces. In addition, the <xref:EnvDTE.OutputWindow> and <xref:EnvDTE.OutputWindowPane> objects add some higher-level functionality to make it easier to enumerate the **Output** window panes and to retrieve text from the panes.  
  
## Creating an Extension that uses the Output Pane  
 You can make an extension that exercises different aspects of the Output pane.  
  
1.  Create a VSIX project named `TestOutput` with a menu command named **TestOutput**. For more information, see [Creating an Extension with a Menu Command](../extensibility/creating-an-extension-with-a-menu-command.md).  
  
2.  Add the following references:  
  
    1.  EnvDTE  
  
    2.  EnvDTE80  
  
3.  In TestOutput.cs, add the following using statement:  
  
    ```f#  
    using EnvDTE;  
    using EnvDTE80;  
    ```  
  
4.  In TestOutput.cs, delete the ShowMessageBox method. Add the following method stub:  
  
    ```c#  
    private void OutputCommandHandler(object sender, EventArgs e)  
    {  
    }  
    ```  
  
5.  In the TestOutput constructor, change the command handler to OutputCommandHandler. Here is the part that adds the commands:  
  
    ```c#  
    OleMenuCommandService commandService = this.ServiceProvider.GetService(typeof(IMenuCommandService)) as OleMenuCommandService;  
    if (commandService != null)  
    {  
        CommandID menuCommandID = new CommandID(MenuGroup, CommandId);  
        EventHandler eventHandler = OutputCommandHandler;  
        MenuCommand menuItem = new MenuCommand(eventHandler, menuCommandID);  
        commandService.AddCommand(menuItem);  
    }  
    ```  
  
6.  The sections below have different methods that show different ways of dealing with the Output pane. You can call these methods to body of the OutputCommandHandler() method. For example, the following code adds the CreatePane() method given in the next section.  
  
    ```c#  
    private void OutputCommandHandler(object sender, EventArgs e)  
    {  
        CreatePane(new Guid(), "Created Pane", true, false);  
    }  
    ```  
  
## Creating an Output Window with IVsOutputWindow  
 This example shows how to create a new **Output** window pane by using the <xref:Microsoft.VisualStudio.Shell.Interop.IVsOutputWindow> interface.  
  
```c#  
void CreatePane(Guid paneGuid, string title,   
    bool visible, bool clearWithSolution)  
{  
    IVsOutputWindow output =   
        (IVsOutputWindow)GetService(typeof(SVsOutputWindow));  
    IVsOutputWindowPane pane;  
  
    // Create a new pane.  
    output.CreatePane(  
        ref paneGuid,   
        title,   
        Convert.ToInt32(visible),   
        Convert.ToInt32(clearWithSolution));  
  
    // Retrieve the new pane.  
    output.GetPane(ref paneGuid, out pane);  
  
     pane.OutputString("This is the Created Pane \n");  
}  
```  
  
 If you add this method to the extension given in the preceding section, when you click the **Invoke TestOutput** command you should see the **Output** window with a header that says **Show output from: CreatedPane** and the words **This is the Created Pane** in the pane itself.  
  
## Creating an Output Window with OutputWindow  
 This example shows how to create an **Output** window pane by using the <xref:EnvDTE.OutputWindow> object.  
  
```c#  
void CreatePane(string title)  
{  
    DTE2 dte = (DTE2)GetService(typeof(DTE));  
    OutputWindowPanes panes =  
        dte.ToolWindows.OutputWindow.OutputWindowPanes;  
  
    try  
    {  
        // If the pane exists already, write to it.  
        panes.Item(title);  
    }  
    catch (ArgumentException)  
    {  
        // Create a new pane and write to it.  
        return panes.Add(title);  
    }  
}  
```  
  
 Although the <xref:EnvDTE.OutputWindowPanes> collection lets you retrieve an **Output** window pane by its title, pane titles are not guaranteed to be unique. When you doubt the uniqueness of a title, use the <xref:Microsoft.VisualStudio.Shell.Interop.IVsOutputWindow.GetPane*> method to retrieve the correct pane by its GUID.  
  
 If you add this method to the extension given in the preceding section, when you click the **Invoke TestOutput** command you should see the Output window with a header that says **Show output from: DTEPane** and the words **Added DTE Pane** in the pane itself.  
  
## Deleting an Output Window  
 This example shows how to delete an **Output** window pane.  
  
```c#  
void DeletePane(Guid paneGuid)  
{  
    IVsOutputWindow output =  
    (IVsOutputWindow)ServiceProvider.GetService(typeof(SVsOutputWindow));  
  
    IVsOutputWindowPane pane;  
    output.GetPane(ref paneGuid, out pane);  
  
    if (pane == null)  
    {  
        CreatePane(paneGuid, "New Pane\n", true, true);  
    }  
     else  
    {  
        output.DeletePane(ref paneGuid);  
    }  
}  
```  
  
 If you add this method to the extension given in the preceding section, when you click the **Invoke TestOutput** command you should see the Output window with a header that says **Show output from: New Pane** and the words **Added Created Pane** in the pane itself. If you click the **Invoke TestOutput** command again, the pane is deleted.  
  
## Getting the General Pane of the Output Window  
 This example shows how to get the built-in **General** pane of the **Output** window.  
  
```c#  
void GetGeneralPane()  
{  
    return (IVsOutputWindowPane)GetService(  
        typeof(SVsGeneralOutputWindowPane));  
}  
```  
  
 If you add this method to the extension given in the preceding section, when you click the **Invoke TestOutput** command you should see that the **Output** window shows the words **Found General pane** in the pane.  
  
## Getting the Build Pane of the Output Window  
 This example shows how to find the Build pane and write to it. Since the Build pane isn’t activated by default, it activates it also.  
  
```c#  
void OutputTaskItemStringExExample(string buildMessage)  
{  
    EnvDTE80.DTE2 dte = (EnvDTE80.DTE2)ServiceProvider.GetService(typeof(EnvDTE.DTE));  
  
    EnvDTE.OutputWindowPanes panes =  
        dte.ToolWindows.OutputWindow.OutputWindowPanes;  
    foreach (EnvDTE.OutputWindowPane pane in panes)  
        {  
            if (pane.Name.Contains("Build"))  
            {  
                pane.OutputString(buildMessage + "\n");  
                pane.Activate();  
                return;  
             }  
        }  
}  
```