---
title: "MSBuild Error MSB3145"
ms.custom: na
ms.date: "10/13/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "MSBuild.GenerateBootstrapper.InvalidUrl"
helpviewer_keywords: 
  - "MSB3145"
ms.assetid: 183d4e7e-bdc6-402f-a1b6-531505be605f
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
# MSBuild Error MSB3145
**MSB3145: Build input parameter '\<property>=\<value>' is not a web url or UNC share.**  
  
 This error occurs when the value of the `SupportUrl`, `ComponentsUrl`, or `ApplicationUrl` project property is not valid. The value must be a valid URI or UNC path.  
  
## See Also  
 [\<PackageFiles> Element](../deployment/-packagefiles--element--bootstrapper-.md)