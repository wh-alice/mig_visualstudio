---
title: "MSBuild Error MSB3177 | testtitle"
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
  - "MSBuild.GenerateManifest.AllowPartiallyTrustedCallers"
helpviewer_keywords: 
  - "MSB3177"
ms.assetid: 0b2417d5-3bc3-4169-b69c-a4a3cbf47882
caps.latest.revision: 6
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
# MSBuild Error MSB3177
**MSB3177: Reference '\<reference>' does not allow partially trusted callers.**  
  
 This warning is generated during application manifest generation when the application is a partially trusted application and if *reference* was added as a project reference, has a strong name, and does not have the APTCA attribute.  
  
### To correct this error  
  
-   Add the APTCA attribute to the referenced assembly, or stop using it, if the former is not possible.  
  
## See Also  
 [\<PackageFiles> Element](../deployment/-packagefiles--element--bootstrapper-.md)