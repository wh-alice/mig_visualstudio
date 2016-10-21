---
title: "Installing VSPackages With Windows Installer | hehe"
ms.custom: ""
ms.date: "10/20/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "installation [Visual Studio SDK], with Windows Installer"
  - "VSPackages, deploying"
ms.assetid: 41d2c72c-0a97-4fcd-b3aa-33a8d3aa962a
caps.latest.revision: 30
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
# Installing VSPackages With Windows Installer
Integrating your VSPackage into [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] requires more than just copying files to a user's computer. Your VSPackage's installer must install the VSPackage and its dependent files, and register and integrate them into [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]. Your VSPackage can take advantage of integration features such as displaying an icon on the [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] splash screen and About dialog box.  
  
 Microsoft Windows Installer files are the recommended way to distribute your VSPackages. Easy-to-use Windows Installer packages can run on any Windows operating system supported by [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]. For more information, see [Windows Installer](http://msdn.microsoft.com/en-us/121be21b-b916-43e2-8f10-8b080516d2a0).  
  
## In This Section  
 [Windows Installer Basics](../extensibility-internals/windows-installer-basics.md)  
 Provides an overview of the Windows Installer.  
  
 [VSPackage Setup Scenarios](../extensibility-internals/vspackage-setup-scenarios.md)  
 Discusses different ways you can support side-by-side installations of both your VSPackages and [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)].  
  
 [Authoring a Windows Installer Package](../extensibility-internals/authoring-a-windows-installer-package.md)  
 Provides an overview of the typical steps installers follow to correctly install and integrate VSPackages into [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)].  
  
 [Detecting System Requirements](../extensibility-internals/detecting-system-requirements.md)  
 Describes how an installer can detect [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] and its components and cancel setup if VSPackage requirements are not met.  
  
 [Component Management](../extensibility-internals/component-management.md)  
 Discusses how to develop an installer that will maintain the integrity of previous product versions.  
  
 [Choosing the Installation Directory for a VSPackage](../extensibility-internals/choosing-the-installation-directory-for-a-vspackage.md)  
 Summarizes the options for locating VSPackages.  
  
 [VSPackage Registration](../extensibility-internals/vspackage-registration.md)  
 Discusses how VSPackages are registered at installation time and why self-registration is a bad idea.  
  
 [Deploying Project Types](../extensibility-internals/deploying-project-types.md)  
 Discusses how to use the new project-type aggregator for managed-code project types.  
  
 [How to: Generate Registry Information for an Installer](../extensibility-internals/how-to--generate-registry-information-for-an-installer.md)  
 Explains how to use RegPkg.exe to generate a registration manifest for a managed VSPackage.  
  
 [Commands That Must Be Run After Installation](../extensibility-internals/commands-that-must-be-run-after-installation.md)  
 Explains how to run post-installation commands to integrate VSPackages into [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)].  
  
 [Uninstalling a VSPackage With Windows Installer](../extensibility-internals/uninstalling-a-vspackage-with-windows-installer.md)  
 Describes the steps your installer must perform when users uninstall your VSPackage.  
  
## Related Sections  
 [Installing VSPackages](../misc/installing-vspackages.md)  
 Discusses how to build and install VSPackages and how to support users who are running multiple versions of [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] at the same time.