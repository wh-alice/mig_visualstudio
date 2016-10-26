---
title: "Troubleshooting VSPackages"
ms.custom: ""
ms.date: "10/25/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "VSPackages, troubleshooting"
  - "debugging, VSPackages"
ms.assetid: 274673e7-72e7-476f-a263-3411b5b874be
caps.latest.revision: 22
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
# Troubleshooting VSPackages
Following are common problems that you might have with your VSPackage and tips to resolve the issues.  
  
### To troubleshoot a VSPackage that keeps Visual Studio from starting  
  
-   Start [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] in safe mode.  
  
     To start [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] in safe mode, at a command prompt, type **devenv.exe /safemode**.  
  
     During this process no VSPackages are loaded except the VSPackages that are included with [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)].  
  
### To troubleshoot a VSPackage that does not load  
  
1.  Make sure that you are using the registry root in which the VSPackage is registered to run, usually the experimental registry root.  
  
     For more information, see [The Experimental Instance](../extensibility/the-experimental-instance.md).  
  
2.  If the VSPackage is targeted to run in the experimental registry root, make sure that you are running the experimental version of [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)].  
  
     To run the experimental version, type the following in a command window: **devenv /rootsuffix exp**.  
  
3.  Check your VSPackage registry entries.  
  
     For more information, see [Registering VSPackages](http://msdn.microsoft.com/en-us/31e6050f-1457-4849-944a-a3c36b76f3dd) and [Managing VSPackages](../extensibility/managing-vspackages.md).  
  
4.  Open the **Output** window of the instance of [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] that is failing to load the VSPackage. Information about why the VSPackage is failing to load may be displayed in that window.  
  
    > [!NOTE]
    >  If you are starting the experimental version of [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] from the [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] integrated development environment (IDE), inspect the **Output** window of both versions.  
  
5.  Examine the activity log.  
  
     For more information, see [How to: Use the Activity Log](../extensibility/how-to--use-the-activity-log.md).  
  
6.  For more information about exceptions thrown by the IDE, click **Exceptions** on the **Debug** menu to enable the exceptions. In the **Exceptions** dialog box select the types of exceptions about which you want more information.  
  
### To troubleshoot a VSPackage that does not register  
  
1.  Make sure that the VSPackage assembly resides in a trusted location. RegPkg cannot register assemblies in an untrusted or partially trusted location, such as a network share in the default .net security configuration. Although a warning appears whenever a user creates a project in an untrusted location, the "do not show this message again" checkbox can prevent this warning from reoccurring.  
  
### To troubleshoot a command that is not visible or that generates an error when you click a command  
  
1.  Merge the new or changed menu commands and those already in the IDE by typing the following at the [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] Command Prompt: **devenv /rootsuffix Exp /setup**.  
  
2.  Make sure that [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] can find UI.dll for your VSPackage.  
  
    1.  Find the CLSID of the VSPackage in the Packages section of the registry:  
  
         HKLM\Software\Microsoft\Visual Studio\\*\<version>*\Packages  
  
    2.  Verify that the path given by the SatelliteDll subkey is correct.  
  
### To troubleshoot a VSPackage that behaves unexpectedly  
  
1.  Set breakpoints in your code.  
  
     Good starting points for debugging are the constructor and the initialization method. You can also set breakpoints in the area you want to evaluate, such as a menu command. To enable breakpoints, you must run under the debugger.  
  
    1.  On the **Project** menu, click **Properties**.  
  
    2.  On the **Property Pages** dialog box, select the **Debug** tab.  
  
    3.  In the **Command line arguments** box, type the root suffix of the development environment that your VSPackage targets. For example, to select the experimental build, type: **/RootSuffix Exp**.  
  
    4.  On the **Debug** menu, click **Start Debugging** or press F5.  
  
        > [!NOTE]
        >  If you are debugging a project, create or load an existing instance of your project now.  
  
2.  Use the activity log.  
  
     Trace VSPackage behavior by writing information to the activity log at key points. This technique is especially useful when you run a VSPackage in a retail environment. For more information, see [How to: Use the Activity Log](../extensibility/how-to--use-the-activity-log.md).  
  
3.  Use public symbols.  
  
     To improve readability while debugging, you can attach symbols to the debugger.  
  
    1.  From the **Tools/Options** menu, navigate to the **Debugging/Symbols** dialog box.  
  
    2.  Add this **Symbol file (.pdb) location**:  
  
         [http://msdl.microsoft.com/download/symbols](http://msdl.microsoft.com/download/symbols)  
  
    3.  To improve performance, specify a symbol cache folder, for example:  
  
        ```  
        C:\symbols  
        ```  
  
### To troubleshoot a missing VSPackage or one of its dependencies  
  
1.  For managed code, make sure that the reference paths are correct.  
  
    1.  On the **Project** menu, click **Properties**.  
  
    2.  Select the **References** tab in the **Property Pages** dialog box and make sure all paths are correct. Alternatively, you can use the **Object Browser** to browse for the referenced objects.  
  
         For managed code, you can use the [Fuslogvw.exe (Assembly Binding Log Viewer)](../Topic/Fuslogvw.exe%20\(Assembly%20Binding%20Log%20Viewer\).md) to display the details of failed assembly loads.  
  
2.  For unmanaged code, find the CLSID of the VSPackage in the [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] CLSID registry node:  
  
     HKLM\Software\Microsoft\Visual Studio\\*\<version>*\CLSID  
  
 Make sure that the InprocServer32 entry has the correct path of the VSPackage dll.  
  
## See Also  
 [VSPackages](../extensibility-internals/vspackages.md)