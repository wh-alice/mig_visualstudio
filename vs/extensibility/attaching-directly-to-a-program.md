---
title: "Attaching Directly to a Program | Microsoft Docs"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "debug engines, attaching to programs"
ms.assetid: ad2b7db8-821c-440c-ba07-c55c6a395e0f
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
# Attaching Directly to a Program
Users who want to debug programs in a process that is already running typically follow this process:  
  
1.  In the IDE, choose the **Debug Processes** command from the **Tools** menu.  
  
     The **Processes** dialog box appears.  
  
2.  Choose a process and click the **Attach** button.  
  
     The **Attach to Process** dialog box appears, listing all debug engines (DEs) installed on the machine.  
  
3.  Specify the DEs to use to debug the selected process, and then click **OK**.  
  
 The debug package starts a debug session and passes the list of DEs to it. The debug session in turn passes this list, along with a callback function, to the selected process, and then asks the process to enumerate its running programs.  
  
 Programmatically, in response to the user request, the debug package instantiates the session debug manager (SDM) and passes the list of selected DEs to it. Along with the list, the debug package passes the SDM an [IDebugEventCallback2](../extensibility/idebugeventcallback2.md) interface. The debug package passes the list of DEs to the selected process by calling [IDebugProcess2::Attach](../extensibility/idebugprocess2--attach.md). The SDM then calls [IDebugProcess2::EnumPrograms](../extensibility/idebugprocess2--enumprograms.md) on the port to enumerate the programs running in the process.  
  
 From this point on, each debug engine is attached to a program exactly as detailed in [Attaching After a Launch](../extensibility/attaching-after-a-launch.md), with two exceptions.  
  
 For efficiency, DEs that are implemented to share an address space with the SDM are grouped so that each DE has a set of programs it will attach to. In this case, [IDebugProcess2](../extensibility/idebugprocess2.md) calls [IDebugEngine2::Attach](../extensibility/idebugengine2--attach.md) and passes it an array of programs to attach to.  
  
 The second exception is that the startup events sent by a DE attaching to a program that is already running do not typically include the entry point event.  
  
## See Also  
 [Sending Startup Events After a Launch](../extensibility/sending-startup-events-after-a-launch.md)   
 [Debugging Tasks](../extensibility/debugging-tasks.md)