---
title: "-InstallVSTemplates (devenv.exe)"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-general"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "Devenv, /InstallVSTemplates switch"
  - "/InstallVSTemplates Devenv switch"
  - "InstallVSTemplates switch"
ms.assetid: 1fb466f6-7955-4535-a840-d93eb8aaa492
caps.latest.revision: 11
ms.author: "kempb"
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
# /InstallVSTemplates (devenv.exe)
Registers project or item templates that are located in *\<Visual Studio installation path>*\Common7\IDE\ProjectTemplates\ or *\<Visual Studio installation path>*\Common7\IDE\ItemTemplates\ so that they can be accessed through the **New Project** and **Add New Item** dialog boxes.  
  
> [!WARNING]
>  This switch is supported only for Visual Studio partner development, and is not available in Express editions. You must run devenv as an administrator in order to use the [/Setup (devenv.exe)](../reference/-setup--devenv.exe-.md) and [/InstallVSTemplates (devenv.exe)](../reference/-installvstemplates--devenv.exe-.md) switches. For more information, see [User Permissions](../ide/user-permissions-and-visual-studio.md).  
  
## Syntax  
  
```  
devenv.exe /InstallVSTemplates  
```  
  
## Remarks  
  
## See Also  
 [NIB: Visual Studio Templates](http://msdn.microsoft.com/en-us/141fccaa-d68f-4155-822b-27f35dd94041)   
 [Devenv Command Line Switches](../reference/devenv-command-line-switches.md)