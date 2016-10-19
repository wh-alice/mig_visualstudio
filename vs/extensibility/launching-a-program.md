---
title: "Launching a Program"
ms.custom: ""
ms.date: "10/18/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "debug engines, launching"
  - "programs, launching"
ms.assetid: 6857e9c6-e44a-468a-afa4-f7c4a0b77844
caps.latest.revision: 21
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
# Launching a Program
Users who want to debug a program can press F5 to run the debugger from the IDE. This begins a series of events that ultimately result in the IDE's connecting to a debug engine (DE), which is in turn connected, or attached, to the program as follows:  
  
1.  The IDE first calls the project package to get the solution's active project debug settings. The settings include the starting directory, the environment variables, the port in which the program will run, and the DE to use to create the program, if specified. These settings are passed to the debug package.  
  
2.  If a DE is specified, the DE calls the operating system to launch the program. As a consequence of launching the program, the program's run-time environment is loaded. For example, if a program is written in MSIL, the common language runtime will be invoked to run the program.  
  
     -or-  
  
     If a DE is not specified, the port calls the operating system to launch the program, which causes the program's run-time environment to be loaded.  
  
    > [!NOTE]
    >  If a DE is used to launch a program, it is likely that the same DE will be attached to the program.  
  
3.  Depending on whether the DE or the port launched the program, the DE or the run-time environment then creates a program description, or node, and notifies the port that the program is running.  
  
    > [!NOTE]
    >  It is recommended that the run-time environment create the program node, because the program node is a lightweight representation of a program that can be debugged. There is no need to load up an entire DE just to create and register a program node. If the DE is designed to run in the process of the IDE, but no IDE is actually running, there needs to be a component that can add a program node to the port.  
  
 The newly created program, along with any other programs, related or unrelated, launched or attached to from the same IDE, compose a debug session.  
  
 Programmatically, when the user first presses **F5**, [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)]'s debug package calls the project package (which is associated with the type of program being launched) through the <xref:Microsoft.VisualStudio.Shell.Interop.IVsDebuggableProjectCfg.DebugLaunch*> method, which in turn fills out a <xref:Microsoft.VisualStudio.Shell.Interop.VsDebugTargetInfo2> structure with the solution's active project debug settings. This structure is passed back to the debug package through a call to the <xref:Microsoft.VisualStudio.Shell.Interop.IVsDebugger2.LaunchDebugTargets2*> method. The debug package then instantiates the session debug manager (SDM), which launches the program being debugged and any associated debug engines.  
  
 One of the arguments passed to the SDM is the GUID of the DE to be used to launch the program.  
  
 If the DE GUID is not `GUID_NULL`, the SDM co-creates the DE, and then calls its [LaunchSuspended](../extensibility/idebugenginelaunch2--launchsuspended.md) method to launch the program. For example, if a program is written in native code, then `IDebugEngineLaunch2::LaunchSuspended` will probably call `CreateProcess` and `ResumeThread` (Win32 functions) to run the program.  
  
 As a consequence of launching the program, the program's run-time environment is loaded. Either the DE or the run-time environment then creates an [IDebugProgramNode2](../extensibility/idebugprogramnode2.md) interface to describe the program and passes this interface to [AddProgramNode](../extensibility/idebugportnotify2--addprogramnode.md) to notify the port that the program is running.  
  
 If `GUID_NULL` is passed, then the port launches the program. Once the program is running, the run-time environment creates an `IDebugProgramNode2` interface to describe the program and passes it to `IDebugPortNotify2::AddProgramNode`. This notifies the port that the program is running. Then the SDM attaches the debug engine to the running program.  
  
## In This Section  
 [Notifying the Port](../extensibility/notifying-the-port.md)  
 Explains what happens after a program is launched and the port is notified.  
  
 [Attaching After a Launch](../extensibility/attaching-after-a-launch.md)  
 Documents when the debug session is ready to attach the DE to the program.  
  
## Related Sections  
 [Debugging Tasks](../extensibility/debugging-tasks.md)  
 Contains links to various debugging tasks, such as launching a program and evaluating expressions.