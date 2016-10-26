---
title: "MSBuild Error MSB1003"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "MSBuild.MissingProjectError"
helpviewer_keywords: 
  - "MSB1003"
ms.assetid: db4aa779-af86-4bb6-b86f-9a31866f70f5
caps.latest.revision: 14
ms.author: "mblome"
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
# MSBuild Error MSB1003
**Specify a project or solution file. The current working directory does not contain a project or solution file.**  
  
 If a project or solution file is not specified on the command line, [!INCLUDE[vstecmsbuild](../extensibility-internals/includes/vstecmsbuild_md.md)] searches the current working directory for a file that has a file extension that ends in "proj" or "sln" and uses that file. The current working directory does not contain a file that has a file extension that ends in "proj" or "sln".  
  
### To correct this error  
  
-   Go to the directory that contains the project file you want to build.  
  
-   Specify either the full or relative path to the project file. For example, type `msbuild c:\myapp\myapp.proj` or `msbuild ..\..\myapp\myapp.proj`  
  
-   If the project or solution file has a file extension that does not end in "proj", change the file extension so that it does end in "proj".  
  
## See Also  
 [Command-Line Reference](../msbuild/msbuild-command-line-reference.md)  
 [MSBuild](../msbuild/msbuild1.md)   
 [Project File Schema Reference](../msbuild/msbuild-project-file-schema-reference.md)