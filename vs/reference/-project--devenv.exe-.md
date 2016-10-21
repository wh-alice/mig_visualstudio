---
title: "-Project (devenv.exe)"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-general"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "/project Devenv switch"
  - "projects [Visual Studio], rebuilding"
  - "projects [Visual Studio], building"
  - "deployment projects, specifying"
  - "project Devenv switch (/project)"
  - "Devenv, /project switch"
  - "projects [Visual Studio], cleaning"
ms.assetid: 8b07859c-3439-436d-9b9a-a8ee744eee30
caps.latest.revision: 11
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
# /Project (devenv.exe)
Identifies a single project within the specified solution configuration to build, clean, rebuild, or deploy.  
  
## Syntax  
  
```  
devenv SolutionName {/build|/clean|/rebuild|/deploy} SolnConfigName   
[/project ProjName] [/projectconfig ProjConfigName]   
```  
  
## Arguments  
 /build  
 Builds the project specified by `/project` `ProjName`.  
  
 /clean  
 Cleans all intermediary files and output directories created during a build.  
  
 /rebuild  
 Cleans then builds the project specified by `/project` `ProjName`.  
  
 /deploy  
 Specifies that the project be deployed after a build or rebuild.  
  
 `SolnConfigName`  
 Required. The name of the solution configuration that will be applied to the solution named in `SolutionName`.  
  
 `SolutionName`  
 Required. The full path and name of the solution file.  
  
 /project `ProjName`  
 Optional. The path and name of a project file within the solution. You can enter a relative path from the `SolutionName` folder to the project file, or the project's display name, or the full path and name of the project file.  
  
 /projectconfig `ProjConfigName`  
 Optional. The name of a project build configuration to be applied to the `/project` named.  
  
## Remarks  
  
-   Must be used part of a `devenv /build`, /`clean`, `/rebuild`, or `/deploy` command.  
  
-   Enclose strings that include spaces in double quotation marks.  
  
-   Summary information for builds, including errors, can be displayed in the **Command** window, or in any log file specified with the `/out` switch.  
  
## Example  
 This example builds the project `CSharpConsoleApp`, using the `Debug` project build configuration within the `Debug` solution configuration of `MySolution`.  
  
```  
devenv "C:\Documents and Settings\someuser\My Documents\Visual Studio\Projects\MySolution\MySolution.sln" /build Debug /project "CSharpWinApp\CSharpWinApp.csproj" /projectconfig Debug   
```  
  
## See Also  
 [Devenv Command Line Switches](../reference/devenv-command-line-switches.md)   
 [/ProjectConfig (devenv.exe)](../reference/-projectconfig--devenv.exe-.md)   
 [/Build (devenv.exe)](../reference/-build--devenv.exe-.md)   
 [/Clean (devenv.exe)](../reference/-clean--devenv.exe-.md)   
 [/Rebuild (devenv.exe)](../reference/-rebuild--devenv.exe-.md)   
 [/Deploy (devenv.exe)](../reference/-deploy--devenv.exe-.md)   
 [/Out (devenv.exe)](../reference/-out--devenv.exe-.md)