---
title: "MSBuild Error MSB3118"
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
  - "MSBuild.GenerateManifest.UseApplicationTrustInvalidFrameworkVersion"
helpviewer_keywords: 
  - "MSB3118"
ms.assetid: 9bf5b430-0cfb-4da5-a7f7-04d69f20cce1
caps.latest.revision: 7
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
# MSBuild Error MSB3118
**MSB3118: Application is set to use application trust, but TargetFrameworkVersion is not v3.5.**  
  
 This error occurs when you set the <xref:Microsoft.Build.Tasks.GenerateApplicationManifest.UseApplicationTrust*> property to `True` and set the <xref:Microsoft.Build.Tasks.GenerateApplicationManifest.TargetFrameworkVersion*> property to a version lower than `v3.5` (for example, `v2.0`).  
  
### To correct this error  
  
-   Set the <xref:Microsoft.Build.Tasks.GenerateApplicationManifest.TargetFrameworkVersion*> property to `v3.5` or higher.  
  
## See Also  
 <xref:Microsoft.Build.Tasks.Deployment.ManifestUtilities.ApplicationManifest.UseApplicationTrust*>   
 <xref:Microsoft.Build.Tasks.GenerateApplicationManifest.UseApplicationTrust*>   
 <xref:Microsoft.Build.Tasks.GenerateApplicationManifest.TargetFrameworkVersion*>   
 <xref:Microsoft.Build.Tasks.Deployment.ManifestUtilities.ApplicationManifest.HostInBrowser*>   
 [Publish Page, Project Designer](../ide-reference/publish-page--project-designer.md)   
 [MSBuild Error MSB3116](../misc/msbuild-error-msb3116.md)   
 [MSBuild Error MSB3117](../misc/msbuild-error-msb3117.md)   
 [MSBuild Error MSB3119](../misc/msbuild-error-msb3119.md)   
 [MSBuild Error MSB3174](../misc/msbuild-error-msb3174.md)   
 [MSBuild Error MSB3185](../misc/msbuild-error-msb3185.md)