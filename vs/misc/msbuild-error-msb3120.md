---
title: "MSBuild Error MSB3120 | testtitle"
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
  - "GenerateManifest.FileAssociationExtensionTooLong"
helpviewer_keywords: 
  - "MSB3120"
ms.assetid: 20bc64f5-aadc-4eec-9915-a87a3d7f81ea
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
# MSBuild Error MSB3120
**MSB3120: File association extension '\<extension>' exceeds the maximum allowed length of \<maximumlength>.**  
  
 The number of characters in the file association extension must not exceed the indicated number.  
  
### To correct this error  
  
-   Set the [ClickOnce Deployment Manifest](../deployment/clickonce-deployment-manifest.md)`extension` attribute to a value that does not contain more characters than the allowed limit for the target operating system.  
  
## See Also  
 [Publish Page, Project Designer](../reference/publish-page--project-designer.md)   
 [ClickOnce Application Manifest](../deployment/clickonce-application-manifest.md)