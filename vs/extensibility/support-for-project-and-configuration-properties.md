---
title: "Support for Project and Configuration Properties"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "project properties, supporting with Visual Studio SDK"
  - "configuration properties, suppporting with Visual Studio SDK"
ms.assetid: 9fcfaa0f-7b41-4b68-82ec-7a151dca5d7e
caps.latest.revision: 25
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
# Support for Project and Configuration Properties
The **Properties** window in the [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] integrated development environment (IDE) can display project and configuration properties. You can provide a property page for your own project type so that the user can set properties for your application.  
  
 By selecting a project node in **Solution Explorer** and then clicking **Properties** on the **Project** menu, you can open a dialog box that includes project and configuration properties. In [!INCLUDE[csprcs](../datatools/includes/csprcs_md.md)] and [!INCLUDE[vbprvb](../codequality/includes/vbprvb_md.md)], and project types derived from these languages, this dialog box appears as a tabbed page in the [General, Environment, Options Dialog Box](../reference/general--environment--options-dialog-box.md). For more information, see [Not in Build: Walkthrough: Exposing Project and Configuration Properties (C#)](http://msdn.microsoft.com/en-us/d850d63b-25e2-4505-9f3d-eb038d7c1d0e).  
  
 The Managed Package Framework for Projects (MPFProj) provides helper classes for creating and managing new project system. You can find the source code and compilation instructions at [MPF for Projects - Visual Studio 2013](http://mpfproj12.codeplex.com/).  
  
## Persistence of Project and Configuration Properties  
 Project and configuration properties are persisted in a project file that has an file name extension associated with the project type, for example, .csproj, .vbproj, and .myproj. Language projects typically use a template file to generate the project file. However, there are actually several ways to associate project types and templates. For more information, see [NIB: Visual Studio Templates](http://msdn.microsoft.com/en-us/141fccaa-d68f-4155-822b-27f35dd94041) and [Template Directory Description (.Vsdir) Files](../extensibility/template-directory-description--.vsdir--files.md).  
  
 Project and configuration properties are created by adding items to the template file. These properties are then available to any project created by using the project type that uses this template. [!INCLUDE[csprcs](../datatools/includes/csprcs_md.md)] projects and the MPFProj both use the [Not in Build: MSBuild Overview](http://msdn.microsoft.com/en-us/b588fd73-a45b-4706-908f-cc131bccfbde) schema for template files. These files have a PropertyGroup section for each configuration. Properties of projects are typically persisted in the first PropertyGroup section, which has a Configuration argument set to a null string.  
  
 The following code shows the start of a basic MSBuild project file.  
  
```  
<Project MSBuildVersion="2.0" DefaultTargets="Build" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
  <PropertyGroup>  
    <Configuration Condition=" '$(Configuration)' == '' ">Debug</Configuration>  
    <Name>SomeProjectSix</Name>  
    <SchemaVersion>2.0</SchemaVersion>  
  </PropertyGroup>  
  <PropertyGroup Condition=" '$(Configuration)' == 'Debug' ">  
    <Optimize>false</Optimize>  
  </PropertyGroup>  
  <PropertyGroup Condition=" '$(Configuration)' == 'Release' ">  
    <Optimize>true</Optimize>  
```  
  
 In this project file, `<Name>` and `<SchemaVersion>` are project properties, and `<Optimize>` is a configuration property.  
  
 It is the responsibility of the project to persist the project and configuration properties of the project file.  
  
> [!NOTE]
>  A project can optimize persistence by persisting only property values that differ from their default values.  
  
## Support for Project and Configuration Properties  
 The `Microsoft.VisualStudio.Package.SettingsPage` class implements project and configuration property pages. The default implementation of `SettingsPage` offers public properties to a user in a generic property grid. The `Microsoft.VisualStudio.Package.HierarchyNode.GetPropertyPageGuids` method selects classes derived from `SettingsPage` for project property grids. The `Microsoft.VisualStudio.Package.ProjectNode.GetConfigPropertyPageGuids` method selects classes derived from `SettingsPage` for configuration property grids. Your project type should override these methods to select the appropriate property pages.  
  
 The `SettingsPage` class and the `Microsoft.VisualStudio.Package.ProjectNode` class offer these methods to persist project and configuration properties:  
  
-   `Microsoft.VisualStudio.Package.ProjectNode.GetProjectProperty` and `Microsoft.VisualStudio.Package.ProjectNode.SetProjectProperty` persist project properties.  
  
-   `Microsoft.VisualStudio.Package.SettingsPage.GetConfigProperty` and `Microsoft.VisualStudio.Package.SettingsPage.SetConfigProperty` persist configuration properties.  
  
    > [!NOTE]
    >  The implementations of the `Microsoft.VisualStudio.Package.SettingsPage` and `Microsoft.VisualStudio.Package.ProjectNode` classes use the `Microsoft.Build.BuildEngine` (MSBuild) methods to get and set project and configuration properties from the project file.  
  
 The class you derive from `SettingsPage` must implement `Microsoft.VisualStudio.Package.SettingsPage.ApplyChanges` and `Microsoft.VisualStudio.Package.SettingsPage.BindProperties` to persist project or configuration properties of the project file.  
  
## ProvideObjectAttribute and Registry Path  
 Classes derived from `SettingsPage` are designed to be shared across VSPackages. To make it possible for a VSPackage to create a class derived from `SettingsPage`, add a `Microsoft.VisualStudio.Shell.ProvideObjectAttribute` to a class derived from `Microsoft.VisualStudio.Shell.Package`.  
  
 [!code[VSSDKSupportProjectConfigurationProperties#1](../extensibility/codesnippet/CSharp/support-for-project-and-configuration-properties_1.cs)]
[!code[VSSDKSupportProjectConfigurationProperties#1](../extensibility/codesnippet/VisualBasic/support-for-project-and-configuration-properties_1.vb)]  
  
 The VSPackage to which the attribute is attached is unimportant. When a VSPackage is registered with [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)], the class id (CLSID) of any object that can be created is registered so that a call to <xref:Microsoft.VisualStudio.Shell.Interop.ILocalRegistry.CreateInstance*> can create it.  
  
 The registry path of an object that can be created is determined by combining <xref:Microsoft.VisualStudio.Shell.Package.UserRegistryRoot*>, the word, CLSID, and the guid of the object type. If `MyProjectPropertyPage` class has a guid of {3c693da2-5bca-49b3-bd95-ffe0a39dd723} and the UserRegistryRoot is HKEY_CURRENT_USER\Software\Microsoft\VisualStudio\8.0Exp, then the registry path would be HKEY_CURRENT_USER\Software\Microsoft\VisualStudio\8.0Exp\CLSID\\{3c693da2-5bca-49b3-bd95-ffe0a39dd723}.  
  
## Project and Configuration Property Attributes and Layout  
 The <xref:System.ComponentModel.CategoryAttribute>, <xref:System.ComponentModel.DisplayNameAttribute>, and <xref:System.ComponentModel.DescriptionAttribute> attributes determine the layout, labeling, and description of project and configuration properties in a generic property page. These attributes determine the category, display name, and description of the option, respectively.  
  
> [!NOTE]
>  Equivalent attributes, SRCategory, LocDisplayName, and SRDescription, use string resources for localization and are defined in [MPF for Projects - Visual Studio 2013](http://mpfproj12.codeplex.com/).  
  
 Consider the following code fragment:  
  
 [!code[VSSDKSupportProjectConfigurationProperties#2](../extensibility/codesnippet/VisualBasic/support-for-project-and-configuration-properties_2.vb)]
[!code[VSSDKSupportProjectConfigurationProperties#2](../extensibility/codesnippet/CSharp/support-for-project-and-configuration-properties_2.cs)]  
  
 The `MyConfigProp` configuration property appears on the configuration property page as **My Config Property** in the category, **My Category**. If the option is selected, the description, **My Description**, appears in the description panel.  
  
## See Also  
 [Not in Build: Walkthrough: Exposing Project and Configuration Properties (C#)](http://msdn.microsoft.com/en-us/d850d63b-25e2-4505-9f3d-eb038d7c1d0e)   
 [Adding and Removing Property Pages](../extensibility/adding-and-removing-property-pages.md)   
 [VSPackage State](../misc/vspackage-state.md)   
 [Projects](../extensibility/projects.md)   
 [NIB: Visual Studio Templates](http://msdn.microsoft.com/en-us/141fccaa-d68f-4155-822b-27f35dd94041)   
 [Template Directory Description (.Vsdir) Files](../extensibility/template-directory-description--.vsdir--files.md)