---
title: "MSBuild Toolset (ToolsVersion)"
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
  - "MSBuild, multitargeting"
  - "targeting a specific .NET framework [MSBuild]"
  - "MSBuild, targeting a specific .NET framework"
  - "multitargeting [MSBuild]"
ms.assetid: 40040ee7-4620-4043-a6d8-ccba921421d1
caps.latest.revision: 30
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
# MSBuild Toolset (ToolsVersion)
MSBuild uses a Toolset of tasks, targets, and tools to build an application. Typically, a MSBuild Toolset includes a microsoft.common.tasks file, a microsoft.common.targets file, and compilers such as csc.exe and vbc.exe. Most Toolsets can be used to compile applications to more than one version of the .NET Framework and more than one system platform. However, the MSBuild 2.0 Toolset can be used to target only the .NET Framework 2.0.  
  
## ToolsVersion Attribute  
 Specify the Toolset in the `ToolsVersion` attribute on the [Project](../reference/project-element--msbuild-.md) element in the project file. The following example specifies that the project should be built by using the MSBuild 12.0 Toolset.  
  
```  
<Project ToolsVersion="12.0" ... </Project>  
```  
  
## How the ToolsVersion Attribute Works  
 When you create a project in Visual Studio, or upgrade an existing project, an attribute named `ToolsVersion` is automatically included in the project file and its value corresponds to the version of MSBuild that is included in the Visual Studio edition. For more information, see [Targeting a Specific .NET Framework Version](../ide/targeting-a-specific-.net-framework-version.md).  
  
 When a `ToolsVersion` value is defined in a project file, MSBuild uses that value to determine the values of the Toolset properties that are available to the project. One Toolset property is `$(MSBuildToolsPath)`, which specifies the path of the .NET Framework tools. Only that Toolset property (or `$(MSBuildBinPath)`), is required.  
  
 Starting in Visual Studio 2013, the MSBuild Toolset version is the same as the Visual Studio version number. MSBuild defaults to this Toolset within Visual Studio and on the command line, regardless of the toolset version specified in project file.  This behavior can be overridden by using the /ToolsVersion flag. For more information, see [Overriding ToolsVersion Settings](../reference/overriding-toolsversion-settings.md).  
  
 In the following example, MSBuild finds the Microsoft.CSharp.targets file by using the `MSBuildToolsPath` reserved property.  
  
```  
<Import Project="$(MSBuildToolsPath)\Microsoft.CSharp.targets" />  
```  
  
 You can modify the value of `MSBuildToolsPath` by defining a custom Toolset. For more information, see [Standard and Custom Toolset Configurations](../reference/standard-and-custom-toolset-configurations.md)  
  
 When you build a solution on the command line and specify a `ToolsVersion` for msbuild.exe, all projects and their project-to-project dependencies are built according to that `ToolsVersion`, even if each project in the solution specifies its own `ToolsVersion`. To define the `ToolsVersion` value on a per project basis, see [Overriding ToolsVersion Settings](../reference/overriding-toolsversion-settings.md).  
  
 The `ToolsVersion` attribute is also used for project migration. For example, if you open a Visual Studio 2008 project in Visual Studio 2010, the project file is updated to include ToolsVersion=”4.0”. If you then try to open that project in Visual Studio 2008, it doesn’t recognize the upgraded `ToolsVersion` and therefore builds the project as though the attribute was still set to 3.5.  
  
 Visual Studio 2010 and Visual Studio 2012 use a ToolsVersion of 4.0. Visual Studio 2013 uses a ToolsVersion of 12.0. In many cases, you can open the project in all three versions of Visual Studio without modification. Visual Studio always uses the correct Toolset, but you will be notified if the version used does not match the version in the project file. In almost all cases, this warning is benign as the Toolsets are compatible in most cases.  
  
 Sub-toolsets, which are described later in this topic, allow MSBuild to automatically switch which set of tools to use based on the context in which the build is being run. For example, MSBuild uses a newer set of tools when it's run in Visual Studio 2012 than when it's run in Visual Studio 2010, without your having to explicitly change the project file. For more information, see [Making Custom Projects Version-Aware](../misc/making-custom-projects-version-aware.md).  
  
## Toolset Implementation  
 Implement a Toolset by selecting the paths of the various tools, targets, and tasks that make up the Toolset. The tools in the Toolset that MSBuild defines come from the following sources:  
  
-   The .NET Framework folder.  
  
-   Additional managed tools.  
  
 The managed tools include ResGen.exe and TlbImp.exe.  
  
 MSBuild provides two ways to access the Toolset:  
  
-   By using Toolset properties  
  
-   By using <xref:Microsoft.Build.Utilities.ToolLocationHelper> methods  
  
 Toolset properties specify the paths of the tools. MSBuild uses the value of the `ToolsVersion` attribute in the project file to locate the corresponding registry key, and then uses the information in the registry key to set the Toolset properties. For example, if `ToolsVersion` has the value `12.0`, then MSBuild sets the Toolset properties according to this registry key: HKLM\Software\Microsoft\MSBuild\ToolsVersions\12.0.  
  
 These are Toolset properties:  
  
-   `MSBuildToolsPath` specifies the path of the MSBuild binaries.  
  
-   `SDK40ToolsPath` specifies the path of additional managed tools for MSBuild 4.x (which could be 4.0 or 4.5).  
  
-   `SDK35ToolsPath` specifies the path of additional managed tools for MSBuild 3.5.  
  
 Alternately, you can determine the Toolset programmatically by calling the methods of the <xref:Microsoft.Build.Utilities.ToolLocationHelper> class. The class includes these methods:  
  
-   <xref:Microsoft.Build.Utilities.ToolLocationHelper.GetPathToDotNetFramework*> returns the path of the .NET Framework folder.  
  
-   <xref:Microsoft.Build.Utilities.ToolLocationHelper.GetPathToDotNetFrameworkFile*> returns the path of a file in the .NET Framework folder.  
  
-   <xref:Microsoft.Build.Utilities.ToolLocationHelper.GetPathToDotNetFrameworkSdk*> returns the path of the managed tools folder.  
  
-   <xref:Microsoft.Build.Utilities.ToolLocationHelper.GetPathToDotNetFrameworkSdkFile*> returns the path of a file, which is typically located in the managed tools folder.  
  
-   <xref:Microsoft.Build.Utilities.ToolLocationHelper.GetPathToBuildTools*> returns the path of the build tools.  
  
### Sub-toolsets  
 As described earlier in this topic, MSBuild uses a registry key to specify the path of the basic tools. If the key has a subkey, MSBuild uses it to specify the path of a sub-toolset that contains additional tools. In this case, the Toolset is defined by combining the property definitions that are defined in both keys.  
  
> [!NOTE]
>  If toolset property names collide, the value that's defined for the subkey path overrides the value that's defined for the root key path.  
  
 Sub-toolsets become active in the presence of the `VisualStudioVersion` build property. This property may take one of these values:  
  
-   “10.0” specifies the .NET Framework 4 sub-toolset  
  
-   “11.0” specifies the .NET Framework 4.5 sub-toolset  
  
-   “12.0” specifies the .NET Framework 4.5.1 sub-toolset  
  
 Sub-toolsets 10.0 and 11.0 should be used with ToolsVersion 4.0. In later versions, the sub-toolset version and the ToolsVersion should match.  
  
 During a build, MSBuild automatically determines and sets a default value for the `VisualStudioVersion` property if it's not already defined.  
  
 MSBuild provides overloads for the `ToolLocationHelper` methods that add a `VisualStudioVersion` enumerated value as a parameter  
  
 Sub-toolsets were introduced in the .NET Framework 4.5.  
  
## See Also  
 [Standard and Custom Toolset Configurations](../reference/standard-and-custom-toolset-configurations.md)   
 [Multitargeting](../reference/msbuild-multitargeting-overview.md)