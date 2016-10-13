---
title: "Creating and Managing Modal Dialog Boxes"
ms.custom: na
ms.date: "10/06/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "dialog boxes, managing in Visual Studio"
ms.assetid: 491bc0de-7dba-478c-a76b-923440e090f3
caps.latest.revision: 10
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
# Creating and Managing Modal Dialog Boxes
When you create a modal dialog box inside Visual Studio, you must make sure that the parent window of the dialog box is disabled while the dialog box is displayed, then re-enable the parent window after the dialog box is closed. If you do not do so, you may receive the error: "Microsoft Visual Studio cannot shut down because a modal dialog is active. Close the active dialog and try again."  
  
 There are two ways of doing this. The recommended way, if you have a WPF dialog box, is to derive it from \<xref:Microsoft.VisualStudio.PlatformUI.DialogWindow>, and then call \<xref:Microsoft.VisualStudio.PlatformUI.DialogWindow.ShowModal*> to display the dialog box. If you do this, you do not need to manage the modal state of the parent window.  
  
 If your dialog box is not WPF, or for some other reason you cannot derive your dialog box class from \<xref:Microsoft.VisualStudio.PlatformUI.DialogWindow>, then you must get the parent of the dialog box by calling \<xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShell.GetDialogOwnerHwnd*> and manage the modal state yourself, by calling the \<xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShell.EnableModeless*> method with a parameter of 0 (false) before displaying the dialog box and calling the method again with a parameter of 1 (true) after closing the dialog box.  
  
## Creating a dialog box derived from DialogWindow  
  
1.  Create a VSIX project named **OpenDialogTest** and add a menu command named **OpenDialog**. For more information about how to do this, see [Creating an Extension with a Menu Command](../extensibility/creating-an-extension-with-a-menu-command.md).  
  
2.  To use the \<xref:Microsoft.VisualStudio.PlatformUI.DialogWindow> class, you must add references to the following assemblies (in the Framework tab of the **Add Reference** dialog box):  
  
    -   PresentationCore  
  
    -   PresentationFramework  
  
    -   WindowsBase  
  
    -   System.Xaml  
  
3.  In OpenDialog.cs, add the following `using` statement:  
  
    ```c#  
    using Microsoft.VisualStudio.PlatformUI;  
    ```  
  
4.  Declare a class named **TestDialogWindow** that derives from \<xref:Microsoft.VisualStudio.PlatformUI.DialogWindow>:  
  
    ```c#  
    class TestDialogWindow : DialogWindow  
    {. . .}  
    ```  
  
5.  To be able to minimize and maximize the dialog box, set \<xref:Microsoft.VisualStudio.PlatformUI.DialogWindowBase.HasMaximizeButton*> and \<xref:Microsoft.VisualStudio.PlatformUI.DialogWindowBase.HasMinimizeButton*> to true:  
  
    ```c#  
    internal TestDialogWindow()  
    {  
        this.HasMaximizeButton = true;  
        this.HasMinimizeButton = true;  
    }  
    ```  
  
6.  In the **OpenDialog.ShowMessageBox** method, replace the existing code with the following:  
  
    ```c#  
    TestDialogWindow testDialog = new TestDialogWindow();  
    testDialog.ShowModal();  
    ```  
  
7.  Build and run the application. The experimental instance of Visual Studio should appear. On the **Tools** menu of the experimental instance you should see a command named **Invoke OpenDialog**. When you click this command, you should see the dialog window. You should be able to minimize and maximize the window.  
  
## Creating and managing a dialog box not derived from DialogWindow  
  
1.  For this procedure, you can use the **OpenDialogTest** solution you created in the previous procedure, with the same assembly references.  
  
2.  Add the following `using` declarations:  
  
    ```c#  
    using System.Windows;  
    using Microsoft.Internal.VisualStudio.PlatformUI;  
    ```  
  
3.  Create a class named **TestDialogWindow2** that derives from \<xref:System.Windows.Window>:  
  
    ```c#  
    class TestDialogWindow2 : Window  
    {. . .}  
    ```  
  
4.  Add a private reference to \<xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShell>:  
  
    ```  
    private IVsUIShell shell;  
    ```  
  
5.  Add a constructor that sets the reference to \<xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShell>:  
  
    ```c#  
    public TestDialogWindow2(IVsUIShell uiShell)  
    {  
        shell = uiShell;  
    }  
    ```  
  
6.  In the **OpenDialog.ShowMessageBox** method, replace the existing code with the following:  
  
    ```c#  
    IVsUIShell uiShell = (IVsUIShell)ServiceProvider.GetService(typeof(SVsUIShell));  
  
    TestDialogWindow2 testDialog2 = new TestDialogWindow2(uiShell);  
    //get the owner of this dialog  
    IntPtr hwnd;  
    uiShell.GetDialogOwnerHwnd(out hwnd);  
    testDialog2.WindowStartupLocation = System.Windows.WindowStartupLocation.CenterOwner;  
    uiShell.EnableModeless(0);  
    try  
    {  
        WindowHelper.ShowModal(testDialog2, hwnd);  
    }  
    finally  
    {  
        // This will take place after the window is closed.  
        uiShell.EnableModeless(1);  
    }  
    ```  
  
7.  Build and run the application. On the **Tools** menu you should see a command named **Invoke OpenDialog**. When you click this command, you should see the dialog window.