---
title: "MSBuild Error MSB2001"
ms.custom: ""
ms.date: "10/20/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "MSBuild.MissingOldProjectFile"
helpviewer_keywords: 
  - "MSB2001"
ms.assetid: af3f4154-7ef3-4903-bde9-b18a66392622
caps.latest.revision: 12
ms.author: "mblome"
manager: "douge"
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
# MSBuild Error MSB2001
**Element \<{0}> does not contain the required attribute "{1}".**  
  
 The project being converted was either modified, corrupted, or not created by [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)].  
  
### To correct this error  
  
-   Check whether the project file has been modified or corrupted. If it has been modified or corrupted, open the project in the version of [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] in which it was created, save it, and then attempt to convert it again.  
  
## See Also  
 [Devenv Command Line Switches](../ide-reference/devenv-command-line-switches.md)   
 [Command-Line Reference](../msbuild/msbuild-command-line-reference.md)