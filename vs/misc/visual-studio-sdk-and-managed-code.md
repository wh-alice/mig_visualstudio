---
title: "Visual Studio SDK and Managed Code"
ms.custom: na
ms.date: "10/13/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "VSIP, about managed code"
ms.assetid: 16b3d88e-b5d8-49a5-a5d7-07cbb0b7e4fc
caps.latest.revision: 20
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
# Visual Studio SDK and Managed Code
*Managed code* is code that is written in any language that targets the common language runtime (CLR), such as [!INCLUDE[vbprvb](../codequality/includes/vbprvb_md.md)], [!INCLUDE[csprcs](../datatools/includes/csprcs_md.md)], or [!INCLUDE[vcprvc](../codequality/includes/vcprvc_md.md)]. Regardless of the language that it is written in, all managed code is compiled into Microsoft Intermediate Language (MSIL) instead of native code.  
  
## Environment Support for Managed VSPackages  
 To support creating a VSPackage or project with a managed language such as [!INCLUDE[csprcs](../datatools/includes/csprcs_md.md)], the [!INCLUDE[vsipsdk](../extensibility/includes/vsipsdk_md.md)] provides the following:  
  
-   The [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] interop assemblies, which enable VSPackages written in managed code to interoperate with the unmanaged (COM) [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] integrated development environment (IDE). For more information, see [Using Visual Studio Interop Assemblies](../extensibility/using-visual-studio-interop-assemblies.md).  
  
-   A set of Managed Package Framework (MPF) classes that provides a higher-level abstraction for working with the [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] IDE. These classes encapsulate some of the most frequently used interfaces and types in the [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] interop assemblies. They greatly reduce the amount of work that you must do to provide the basic functionality of a VSPackage or project. For more information, see [Managed Package Framework Classes](../misc/managed-package-framework-classes.md).  
  
-   A set of basic VSPackage samples written in managed code. The managed samples build on an example of a simple, fully functional VSPackage to demonstrate a basic editor, a tool window, an object extender, and other components. For more information, see [VSSDK Samples](../misc/vssdk-samples.md).  
  
## See Also  
 [Managed VSPackages](../misc/managed-vspackages.md)   
 [Using Visual Studio Interop Assemblies](../extensibility/using-visual-studio-interop-assemblies.md)   
 [Managed Package Framework Classes](../misc/managed-package-framework-classes.md)