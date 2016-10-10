---
title: "WPF MSBuild Task Reference"
ms.custom: na
ms.date: "10/04/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: na
ms.topic: "article"
dev_langs: 
  - "VB"
  - "CSharp"
  - "C++"
  - "jsharp"
helpviewer_keywords: 
  - "WPF MSBuild task reference [WPF MSBuild], term/definition table"
  - "build tasks [WPF MSBuild], Microsoft build engine"
  - "build tasks using the Microsoft build engine [WPF MSBuild], compile markup and process resources"
  - "WPF MSBuild task reference [WPF MSBuild]"
ms.assetid: 96df0370-e50f-4ffc-9771-b12fb8721143
caps.latest.revision: 4
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
# WPF MSBuild Task Reference
The Windows Presentation Foundation (WPF) build process extends Microsoft build engine (MSBuild) with an additional set of build tasks, including tasks to compile markup and process resources.  
  
## In This Section  
 [FileClassifier](../VS_IDE/fileclassifier-task.md)  
 Classifies a set of source resources as those that will be embedded into an assembly. If a resource is not localizable, it is embedded into the main application assembly; otherwise, it is embedded into a satellite assembly.  
  
 [GenerateTemporaryTargetAssembly](../VS_IDE/generatetemporarytargetassembly-task.md)  
 Generates an assembly if at least one [!INCLUDE[TLA#tla_xaml](../VS_IDE/includes/tlasharptla_xaml_md.md)] page in a project references a type that is declared locally in that project. The generated assembly is removed after the build process is completed, or if the build process fails.  
  
 [GetWinFXPath](../VS_IDE/getwinfxpath-task.md)  
 Returns the directory of the current [!INCLUDE[TLA#tla_winfx](../VS_IDE/includes/tlasharptla_winfx_md.md)] runtime.  
  
 [MarkupCompilePass1](../VS_IDE/markupcompilepass1-task.md)  
 Converts non-localizable [!INCLUDE[TLA#tla_xaml](../VS_IDE/includes/tlasharptla_xaml_md.md)] project files to compiled binary format.  
  
 [MarkupCompilePass2](../VS_IDE/markupcompilepass2-task.md)  
 Performs second-pass markup compilation on [!INCLUDE[TLA#tla_xaml](../VS_IDE/includes/tlasharptla_xaml_md.md)] files that reference types in the same project.  
  
 [MergeLocalizationDirectives](../VS_IDE/mergelocalizationdirectives-task.md)  
 Merges the localization attributes and comments of one or more [!INCLUDE[TLA2#tla_xaml](../VS_IDE/includes/tla2sharptla_xaml_md.md)] binary format files into a single file for the whole assembly.  
  
 [ResourcesGenerator](../VS_IDE/resourcesgenerator-task.md)  
 Embeds one or more resources (.jpg, .ico, .bmp, [!INCLUDE[TLA2#tla_xaml](../VS_IDE/includes/tla2sharptla_xaml_md.md)] in binary format, and other extension types) into a .resources file.  
  
 [UidManager](../VS_IDE/uidmanager-task.md)  
 Checks, updates, or removes unique identifiers (UIDs), in order to localize all [!INCLUDE[TLA#tla_xaml](../VS_IDE/includes/tlasharptla_xaml_md.md)] elements that are included in the source [!INCLUDE[TLA2#tla_xaml](../VS_IDE/includes/tla2sharptla_xaml_md.md)] files.  
  
 [UpdateManifestForBrowserApplication](../VS_IDE/updatemanifestforbrowserapplication-task.md)  
 Adds the **\<hostInBrowser />** element to the application manifest (*projectname*.exe.manifest) when a [!INCLUDE[TLA#tla_xbap](../VS_IDE/includes/tlasharptla_xbap_md.md)] project is built.  
  
## See Also  
 [MSBuild](assetId:///7c49aba1-ee6c-47d8-9de1-6f29a906e20b)