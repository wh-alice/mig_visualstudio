---
title: "MSBuild Error MSB3157"
ms.custom: na
ms.date: "10/01/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "vsdeploy.chm:13157"
  - "MSBuild.GenerateBootstrapper.UsingProductCulture"
helpviewer_keywords: 
  - "MSB3157"
ms.assetid: ccfcbea4-eb9b-42ae-9908-47079ecc84a7
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
# MSBuild Error MSB3157
**MSB3157: Could not match culture '\<culture>' for item '\<package>'. Using culture '\<culture>' instead.**  
  
 This warning is generated when the specified product cannot find a package manifest file (package.xml) that uses the specified culture.  
  
### To correct this error  
  
-   Provide the appropriate package manifest file.  
  
## See Also  
 [\<PackageFiles> Element](../VS_IDE/-packagefiles--element--bootstrapper-.md)