---
title: "MSBuild .Targets Files"
ms.custom: ""
ms.date: "10/20/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
  - "CSharp"
  - "C++"
  - "jsharp"
helpviewer_keywords: 
  - ".Targets files"
  - "MSBuild, .Targets files"
ms.assetid: f6d98eb4-d2fa-49b7-8e3c-bae1ca3cf596
caps.latest.revision: 16
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
# MSBuild .Targets Files
[!INCLUDE[vstecmsbuild](../extensibility-internals/includes/vstecmsbuild_md.md)] includes several .targets files that contain items, properties, targets, and tasks for common scenarios. These files are automatically imported into most [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] project files to simplify maintenance and readability.  
  
 Projects typically import one or more .targets files to define their build process. For example a [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] project created by [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] will import Microsoft.CSharp.targets which imports Microsoft.Common.targets. The [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] project itself will define the items and properties specific to that project, but the standard build rules for a [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] project are defined in the imported .targets files.  
  
 The `$(MSBuildToolsPath)` value specifies the path of these common .targets files. If the `ToolsVersion` is 4.0, the files are in the following location: `WindowsInstallationPath\Microsoft.NET\Framework\v4.0.30319\`  
  
> [!NOTE]
>  For information about how to create your own targets, see [Targets](../reference/msbuild-targets.md). For information about how to use the `Import` element to insert a project file into another project file, see [Import Element (MSBuild)](../reference/import-element--msbuild-.md) and [How to: Use the Same Target in Multiple Project Files](../reference/how-to--use-the-same-target-in-multiple-project-files.md).  
  
## Common .Targets Files  
  
|.Targets file|Description|  
|-------------------|-----------------|  
|Microsoft.Common.targets|Defines the steps in the standard build process for [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] and [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] projects.<br /><br /> Imported by the Microsoft.CSharp.targets and Microsoft.VisualBasic.targets files, which include the following statement: `<Import Project="Microsoft.Common.targets" />`|  
|Microsoft.CSharp.targets|Defines the steps in the standard build process for Visual C# projects.<br /><br /> Imported by Visual C# project files (.csproj), which include the following statement: `<Import Project="$(MSBuildToolsPath)\Microsoft.CSharp.targets" />`|  
|Microsoft.VisualBasic.targets|Defines the steps in the standard build process for Visual Basic projects.<br /><br /> Imported by Visual Basic project files (.vbproj), which include the following statement: `<Import Project="$(MSBuildToolsPath)\Microsoft.VisualBasic.targets" />`|  
  
## See Also  
 [Import Element (MSBuild)](../reference/import-element--msbuild-.md)   
 [MSBuild Reference](../reference/msbuild-reference.md)
 [MSBuild](../reference/msbuild1.md)