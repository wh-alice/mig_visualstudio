---
title: "Project Settings for a Visual Basic Debug Configuration | Microsoft Docs"
ms.custom: ""
ms.date: "10/21/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbProjectPropertiesDebug"
dev_langs: 
  - "FSharp"
  - "VB"
  - "CSharp"
  - "C++"
helpviewer_keywords: 
  - "project settings [Visual Studio], debug configurations"
  - "debug builds, project settings"
  - "debugging [Visual Basic], debugger settings"
  - "projects [Visual Studio], debug configurations"
  - "project configurations, debug"
  - "debug configurations, Visual Basic"
ms.assetid: 72a8483a-af0b-4403-8b0d-ee9ad71ee435
caps.latest.revision: 17
ms.author: "mikejo"
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
# Project Settings for a Visual Basic Debug Configuration
You can change the project settings for a [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] debug configuration in the **Property Pages** window, as discussed in [Debug and Release Configurations](../debugger/how-to--set-debug-and-release-configurations.md). The following tables show where to find debugger-related settings in the **Property Pages** window.  
  
> [!WARNING]
>  This topic does not apply to Store apps. See [Start a debug session (VB, C#, C++ and XAML)](../debugger/66ec0e79-8261-4c19-a618-3fd1b3f71bbd.md)  
  
### Debug tab  
  
|Setting|Description|  
|-------------|-----------------|  
|**Configuration**|Sets mode for compiling the application. Choose among **Active (Debug)**, **Debug**, **Release**, **All Configurations**.|  
|**Start Action**|This group of controls specifies the action that will occur when you choose Start from the Debug menu.<br /><br /> -   **Start project** is the default and launches the startup project for debugging. For more information, see [NIB How to: Set Startup Projects](http://msdn.microsoft.com/en-us/31465836-0911-48db-a5d9-e456b635e970).<br />-   **Start external program** enables you to start and attach to a program that is not part of a [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] project. For more information, see [Attach to Running Processes](../debugger/attach-to-running-processes-with-the-visual-studio-debugger.md).<br />-   **Start browser in URL** enables you to debug a Web application.|  
|**Command Line Arguments**|Specifies command-line arguments for the program to be debugged. The command name is the program name specified in Start external program. If Start Action is set to Start URL, command-line arguments are ignored.|  
|**Working Directory**|Specifies the working directory of the program being debugged. In [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)], the working directory is the directory the application is launched from. The default working directory is \bin\Debug or \bin\Release, depending on the current configuration.|  
|**Use Remote Machine**|When the check box is selected, remote debugging is enabled. In the textbox, you can type name of a remote machine where the application will run for debugging purposes or an [Msvsmon server name](../Topic/Start%20%20the%20Remote%20Debugging%20Monitor.md). The location of the EXE on the remote machine is specified by the Output Path property in the Build tab. The location must be a shareable directory on the remote machine.|  
|**Unmanaged code debugging**|Enables you to debug calls to native (unmanaged) Win32 code from your managed application. This has the same effect as selecting Mixed for Debugger Type in a [!INCLUDE[vcprvc](../code-quality/includes/vcprvc_md.md)] project.|  
|**SQL Server debugging**|Allows debugging of SQL Server database objects.|  
  
### Compile tab: press Advanced Compile Options button  
  
|Setting|Description|  
|-------------|-----------------|  
|**Enable optimizations**|This option should be unchecked. Optimization causes the code that is actually executed to be different from the source code seen in [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)], and thus makes debugging difficult. If code is optimized, symbols are not be loaded by default when debugging with Just My Code.|  
|**Generate debug info**|Defined by default in both debug and release versions, this setting (equivalent to the /debug compiler option) creates debug information at build time. The debugger uses this information to show variable names and other information in a useful form when you are debugging. If you compile your program without this information, debugger functionality will be limited. For more information, see [/debug](../Topic/-debug%20\(Visual%20Basic\).md).|  
|**Define DEBUG Constant**|Defining this symbol enables conditional compiling of output functions from the [Debug class](https://msdn.microsoft.com/en-us/library/system.diagnostics.debug.aspx). With this symbol defined, Debug class methods generate output to the [Output window](../reference/output-window.md). Without this symbol, Debug class methods are not compiled and no output is generated. This symbol should be defined in the Debug version and not defined in the Release version. Defining this symbol in a Release version creates unnecessary code that slows your program down.|  
|**Define TRACE Constant**|Defining this symbol enables conditional compiling of output functions from the [Trace class](https://msdn.microsoft.com/en-us/library/system.diagnostics.trace.aspx). With this symbol defined, the Trace class methods generate output to the [Output window](../reference/output-window.md). Without this symbol, Trace class methods are not compiled and no Trace output is generated. This symbol is defined by default for both Debug and Release versions.|  
  
## See Also  
 [Debugger Settings and Preparation](../debugger/debugger-settings-and-preparation.md)