---
title: "MSBuild Error MSB2009"
ms.custom: na
ms.date: "10/12/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "MSBuild.UnrecognizedAttribute"
helpviewer_keywords: 
  - "MSB2009"
ms.assetid: 34fd83b4-dead-49e5-b1ee-b23dc5a95244
caps.latest.revision: 10
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
# MSBuild Error MSB2009
**Attribute '\<attribute name>' of element '\<element name>' is not valid.**  
  
 The attribute name is not spelled correctly or is not recognized by [!INCLUDE[vstecmsbuild](../extensibility/includes/vstecmsbuild_md.md)].  
  
### To correct this error  
  
-   Check the spelling of the attribute name.  
  
-   Check whether the project file has been modified or corrupted. If it has been modified or corrupted, open the project in the version of [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] in which it was created, save it, and then attempt to convert it again.  
  
## See Also  
 [Project File Schema Reference](../reference/msbuild-project-file-schema-reference.md)