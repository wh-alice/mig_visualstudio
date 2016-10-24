---
title: "MSBuild Error MSB3256 | testtitle"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "MSB3256"
ms.assetid: 809ccd0a-78cd-4bf5-83a8-2fb51815ea27
caps.latest.revision: 11
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
# MSBuild Error MSB3256
**MSB3256: No assemblies were read in from the redist lists. A TargetFramework subset exclusion list could not be generated.**  
  
 A list of redistributable items (redist list) could not be found.  
  
 To generate a list of assemblies to exclude from the .NET Framework subset, two files are required: a "redist list" named FrameworkList.xml, which contains the names of redistributable items in the .NET Framework, and a "subset list" named client.xml, which contains the names of items in the .NET Framework. Because the subset definition requires both lists, if the redist list is missing, then the .NET Framework subset cannot be targeted.  
  
 The [!INCLUDE[net_client_v35_long](../misc/includes/net_client_v35_long_md.md)] is a subset of the full [!INCLUDE[net_v35_short](../misc/includes/net_v35_short_md.md)] run-time library. For more information about the [!INCLUDE[net_client_v35_long](../misc/includes/net_client_v35_long_md.md)], see [.NET Framework Client Profile](../Topic/.NET%20Framework%20Client%20Profile.md).  
  
### To correct this error  
  
-   Either provide a valid redist list named FrameworkList.xml, or target the full [!INCLUDE[net_v35_short](../misc/includes/net_v35_short_md.md)] redistributable library. For information about how to target the full [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)], see [How to: Target a Version of the .NET Framework](../ide/how-to--target-a-version-of-the-.net-framework.md).  
  
## See Also  
 [Target Framework and Target Platform](../reference/msbuild-target-framework-and-target-platform.md)   
 [Project Element (MSBuild)](../reference/project-element--msbuild-.md)   
 [Additional Resources](../reference/additional-msbuild-resources.md)