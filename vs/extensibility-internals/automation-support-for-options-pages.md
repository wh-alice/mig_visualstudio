---
title: "Automation Support for Options Pages"
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
  - "Tools Options pages [Visual Studio SDK], automation support"
  - "automation [Visual Studio SDK], creating Tools Options pages"
ms.assetid: 0b25b82c-7432-4e0a-9e84-350269ba8260
caps.latest.revision: 29
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
# Automation Support for Options Pages
VSPackages can provide custom **Options** dialog boxes to the **Tools** menu (Tools Options pages) in [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] and can make them available to the automation model.  
  
## Tools Options Pages  
 To create a **Tools Options** page, a VSPackage must provide a user control implementation returned to the environment through the VSPackage's implementation of the <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.GetPropertyPage*> method, (or for managed-code the <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.GetPropertyPage*> method).  
  
 It is optional, but strongly encouraged, to allow access to this new page through the automation model. You can do this through the following steps:  
  
1.  Extend the <xref:EnvDTE._DTE.Properties*> object through the implementation of an IDispatch-derived object.  
  
2.  Return an implementation of the <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.GetAutomationObject*> method (or for managed code the <xref:Microsoft.VisualStudio.Shell.Package.GetAutomationObject*> method) to the IDispatch-derived object.  
  
3.  When an automation consumer calls the <xref:EnvDTE._DTE.Properties*> method on a custom **Option** property page, the environment uses the <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.GetAutomationObject*> method to obtain a custom **Tools Options** page's automation implementation.  
  
4.  The automation object of the VSPackage is then used to provide each <xref:EnvDTE.Property> returned by <xref:EnvDTE._DTE.Properties*>.  
  
 For a sample implementing a custom Tools Options page, see [VSSDK Samples](../misc/vssdk-samples.md).  
  
## See Also  
 [Exposing Project Objects](../extensibility-internals/exposing-project-objects.md)