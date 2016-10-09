---
title: "-Deploy (devenv.exe)"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-general"
ms.tgt_pltfrm: na
ms.topic: "article"
H1: "/Deploy (devenv.exe)"
helpviewer_keywords: 
  - "Devenv, /deploy switch"
  - "deploy Devenv switch"
  - "deploying applications [Visual Studio], after build"
  - "/deploy Devenv switch"
ms.assetid: e47c8723-df08-4645-aa2d-0c956e7ccca2
caps.latest.revision: 13
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
# -Deploy (devenv.exe)
Deploys a solution after a build or rebuild. Applies to managed code projects only.  
  
## Syntax  
  
```  
devenv SolutionName /deploy SolnConfigName [/project ProjName] [/projectconfig ProjConfigName] [/out LogFileName]  
```  
  
## Arguments  
 `SolnConfigName`  
 Required. The name of the solution configuration that will be used to build the solution named in `SolutionName`.  
  
 `SolutionName`  
 Required. The full path and name of the solution file.  
  
 /project `ProjName`  
 Optional. The path and name of a project file within the solution. You can enter a relative path from the `SolutionName` folder to the project file, or the project's display name, or the full path and name of the project file.  
  
 /projectconfig `ProjConfigName`  
 Optional. The name of a project build configuration to be used when building the `/project` named.  
  
## Remarks  
 The specified project must be a deployment project. If the specified project is not a deployment project, when the project that has been built is passed to be deployed, it fails with an error.  
  
 Enclose strings that include spaces in double quotation marks.  
  
 Summary information for builds, including errors, can be displayed in the **Command** window, or in any log file specified with the `/out` switch.  
  
## Example  
 This example deploys the project `CSharpConsoleApp`, using the `Release` project build configuration within the `Release` solution configuration of `MySolution`.  
  
```  
devenv "C:\Documents and Settings\someuser\My Documents\Visual Studio\Projects\MySolution\MySolution.sln" /deploy Release /project "CSharpWinApp\CSharpWinApp.csproj" /projectconfig Release   
```  
  
## See Also  
 [Devenv Command Line Switches](../VS_IDE/devenv-command-line-switches.md)   
 [/Project (devenv.exe)](../VS_IDE/-project--devenv.exe-.md)   
 [/Build (devenv.exe)](../VS_IDE/-build--devenv.exe-.md)   
 [/Clean (devenv.exe)](../VS_IDE/-clean--devenv.exe-.md)   
 [/Rebuild (devenv.exe)](../VS_IDE/-rebuild--devenv.exe-.md)   
 [/Out (devenv.exe)](../VS_IDE/-out--devenv.exe-.md)