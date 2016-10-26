---
title: "Configure Firewall for Remote Debugging Dialog Box"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vs.debug.firewallconfiguration"
dev_langs: 
  - "FSharp"
  - "VB"
  - "CSharp"
  - "C++"
  - "JScript"
helpviewer_keywords: 
  - "Configure Firewall for Remote Debugging dialog box"
  - "remote debugging, configuring firewalls"
  - "firewalls, configuring for remote debugging"
ms.assetid: 5dff3393-fdeb-4129-a2f6-31f653107a82
caps.latest.revision: 11
ms.author: "mikejo"
manager: "ghogen"
translation.priority.ht: 
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "ru-ru"
  - "zh-cn"
  - "zh-tw"
translation.priority.mt: 
  - "cs-cz"
  - "pl-pl"
  - "pt-br"
  - "tr-tr"
---
# Configure Firewall for Remote Debugging Dialog Box
This dialog box appears when the Windows Firewall blocks the debugger from receiving information over the network. To continue remote debugging, you must open a hole in the firewall so the debugger can receive information.  
  
> [!CAUTION]
>  Opening a hole in the Firewall may expose your machine to security threats that the Firewall is designed to block. Opening a hole for remote debugging unblocks ports 4020 and 4021 in Visual Studio 2015. In other versions of Visual Studio, other port numbers are used. For more information, see [Remote Debugger Port Assignments](../debugger/remote-debugger-port-assignments.md). In addition, it allows the debugger to open additional ports. For more information, see [Configure the Windows Firewall for Remote Debugging](../debugger/configure-the-windows-firewall-for-remote-debugging.md).  
  
## UIElement List  
 **Cancel remote debugging**  
 Cancels the remote debugging attempt. The security settings of your machine remain intact.  
  
 **Unblock remote debugging from computers on the local network (subnet)**  
 Enables remote debugging of machines on your local subnet. This may open vulnerabilities to machines on your local subnet, but the firewall continues to block information coming from outside the subnet.  
  
 **Unblock remote debugging from any computer**  
 Enables remote debugging of machines anywhere on the network. This setting is the least secure.  
  
## See Also  
 [Debugger Security](../debugger/debugger-security.md)   
 [Set Up the Remote Tools on the Device](../Topic/Set%20Up%20the%20Remote%20Tools%20on%20the%20Device.md)   
 [Debugging User Interface Reference](../debugger/debugging-user-interface-reference.md)