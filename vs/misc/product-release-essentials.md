---
title: "Product Release Essentials"
ms.custom: ""
ms.date: "10/18/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "deployment, essentials"
  - "installation [Visual Studio SDK], essentials"
ms.assetid: 28370bc8-f3a7-4c5e-9b35-8331cda14ff4
caps.latest.revision: 12
manager: "douge"
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
# Product Release Essentials
A pleasant and robust setup experience forms a lasting impression in your users’ minds about your [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] integration product. An unpleasant setup experience also forms a lasting impression, so following best practices in setup development and testing is worth the investment.  
  
## Developing Windows Installer Setup Packages  
 Windows Installer is the recommended installation and configuration service for Windows and for [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] integration products.  
  
> [!NOTE]
>  The [!INCLUDE[vsipsdk](../extensibility/includes/vsipsdk_md.md)] documentation on installing [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] integration products builds on Windows Installer concepts, but it does not cover Windows Installer itself. For links to relevant sections of the Windows Installer documentation, refer to the table below.  
  
 In the context of setup, *component* refers to a Windows Installer component. Components contain resources like files and registry entries, and are installed and removed as a unit.  
  
|Task|For more information, see|  
|----------|-------------------------------|  
|Learn more about Windows Installer.|[Windows Installer](http://msdn.microsoft.com/library/aa372866.aspx)|  
|Determine your VSPackage's system requirements.|-   [Detecting System Requirements](../extensibility/detecting-system-requirements.md)|  
|Learn how to register a VSPackage in a setup package.|-   [VSPackage Registration](../extensibility/vspackage-registration.md)<br />-   [Commands That Must Be Run After Installation](../extensibility/commands-that-must-be-run-after-installation.md)|  
|See a sample installation package.|-   IronPython Integration Setup Sample|  
  
## Supporting Side-by-Side Products  
 Side-by-side (sometimes shortened to *SxS*) refers to the ability to have multiple versions of the same product installed, and even running, simultaneously. For [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] integration products, it also refers to the fact that [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] itself supports side-by-side execution.  
  
|Task|For more information, see|  
|----------|-------------------------------|  
|Learn about supporting multiple versions of [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] in your [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] integration product.|-   [Choosing Between Shared and Versioned VSPackages](../extensibility/choosing-between-shared-and-versioned-vspackages.md)<br />-   [Component Management](../extensibility/component-management.md)|  
|Learn about supporting multiple versions of your [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] integration product.|-   [Choosing Between Shared and Versioned VSPackages](../extensibility/choosing-between-shared-and-versioned-vspackages.md)<br />-   [Registering File Name Extensions for Side-By-Side Deployments](../extensibility/registering-file-name-extensions-for-side-by-side-deployments.md)<br />-   [Detecting System Requirements](../extensibility/detecting-system-requirements.md)<br />-   [Commands That Must Be Run After Installation](../extensibility/commands-that-must-be-run-after-installation.md)|  
  
## Testing Your Visual Studio Integration Product  
 The [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] Integration Test (VSIT) suite is a series of tests that verifies that a VSPackage correctly integrates into [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)]. VSIT does not test a VSPackage’s functionality, but helps ensure that a VSPackage does not adversely affect other [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] functionality. For more information, see [Visual Studio Integration Tests](http://msdn.microsoft.com/en-us/8d741735-7d93-46c2-ab93-01da7a0e016d).