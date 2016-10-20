---
title: "Troubleshooting .NET Framework Targeting Errors | Microsoft Docs"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vs.FrameworkTargetingErrors"
  - "MSBuild.ResolveAssemblyReference.FailedToResolveReferenceBecausePrimaryAssemblyInExclusionList"
helpviewer_keywords: 
  - "targeting .NET Framework version [Visual Studio]"
  - "versions [Visual Studio], .NET Framework Client Profile"
  - "multi-targeting"
  - "multitargeting"
  - ".NET Framework Client Profile"
ms.assetid: 830e3e45-9a93-4279-a249-75b84599aefb
caps.latest.revision: 29
ms.author: "kempb"
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
# Troubleshooting .NET Framework Targeting Errors
This topic describes MSBuild errors that might occur because of reference issues and how you can resolve those errors.  
  
## You Have Referenced a Project or Assembly That Targets a Different Version of the .NET Framework  
 You can create applications that reference projects or assemblies that target different versions of the [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)]. For example, you can create an application that targets the client profile for the [!INCLUDE[net_v40_short](../code-quality/includes/net_v40_short_md.md)] but references an assembly that targets the .NET Framework 2.0. However, if you create a project that targets an earlier version of the [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)], you can’t set a reference in that project to a project or assembly that targets the client profile for the [!INCLUDE[net_v40_short](../code-quality/includes/net_v40_short_md.md)] or the [!INCLUDE[net_v40_short](../code-quality/includes/net_v40_short_md.md)] itself. To resolve the error, make sure that your application targets a profile or profiles that are compatible with the profile that’s targeted by the projects or assemblies that your application references.  
  
## You Have Re-Targeted a Project to a Different Version of the .NET Framework  
 If you change the target version of the [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] for your application, Visual Studio changes some of the references, but you may have to update some references manually. For example, one of the previously mentioned errors might occur if you change an application to target the [!INCLUDE[net_v35SP1_long](../reference/includes/net_v35sp1_long_md.md)] and that application has resources or settings that rely on the client profile for the [!INCLUDE[net_v40_short](../code-quality/includes/net_v40_short_md.md)].  
  
 To work around application settings, open **Solution Explorer**, choose **Show All Files**, and then edit the app.config file in the XML editor of Visual Studio. Change the version in the settings to match the appropriate version of the .NET Framework. For example, you can change the version setting from 4.0.0.0 to 2.0.0.0. Similarly, for an application that has added resources, open **Solution Explorer**, choose the **Show All Files** button, expand **My Project** (Visual Basic) or **Properties** (C#), and then edit the Resources.resx file in the XML editor of Visual Studio. Change the version setting from 4.0.0.0 to 2.0.0.0.  
  
 If your application has resources such as icons or bitmaps or settings such as data connection strings, you can also resolve the error by removing all the items on the **Settings** page of the **Project Designer** and then re-adding the required settings.  
  
## You Have Re-Targeted a Project to a Different Version of the .NET Framework and References Do Not Resolve  
 If you retarget a project to a different version of the [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)], your references may not resolve properly in some cases. Explicit fully qualified references to assemblies often cause this issue, but you can resolve it by removing the references that do not resolve and then adding them back to the project. As an alternative, you can edit the project file to replace the references. First, you remove references of the following form:  
  
```  
<Reference Include="System.ServiceModel, Version=3.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089, processorArchitecture=MSIL" />  
```  
  
 Then you replace them with the simple form:  
  
```  
<Reference Include="System.ServiceModel" />  
```  
  
> [!NOTE]
>  After you close and reopen your project, you should also rebuild it to ensure that all references resolve correctly.  
  
## See Also  
 [How to: Target a Version of the .NET Framework](../ide/how-to--target-a-version-of-the-.net-framework.md)   
 [.NET Framework Client Profile](../Topic/.NET%20Framework%20Client%20Profile.md)   
 [Targeting a Specific .NET Framework Version](../ide/targeting-a-specific-.net-framework-version.md)   
 [Multitargeting](../reference/msbuild-multitargeting-overview.md)