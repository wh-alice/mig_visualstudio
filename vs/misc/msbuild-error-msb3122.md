---
title: "MSBuild Error MSB3122"
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
  - "GenerateManifest.FileAssociationsApplicationNotFullTrust"
helpviewer_keywords: 
  - "MSB3122"
ms.assetid: 523e4160-f165-437a-9f19-fb2ec77d46f5
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
# MSBuild Error MSB3122
**MSB3122: Use of file associations requires full trust.**  
  
 Publishing an application that configures file associations requires that the application be a full trust application.  
  
### To correct this error  
  
-   Enable ClickOnce security settings and set the application to a full trust application. For more information, see [How to: Enable ClickOnce Security Settings](../deployment/how-to--enable-clickonce-security-settings.md).  
  
## See Also  
 [Publish Page, Project Designer](../ide/reference/publish-page--project-designer.md)   
 [ClickOnce Application Manifest](../deployment/clickonce-application-manifest.md)   
 [Code Access Security for ClickOnce Applications](../deployment/code-access-security-for-clickonce-applications.md)