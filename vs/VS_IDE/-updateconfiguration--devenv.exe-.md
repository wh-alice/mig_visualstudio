---
title: "-Updateconfiguration (devenv.exe)"
ms.custom: na
ms.date: "10/04/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-general"
ms.tgt_pltfrm: na
ms.topic: "article"
H1: "/Updateconfiguration (devenv.exe)"
helpviewer_keywords: 
  - "/updateconfiguration Devenv switch"
  - "Devenv, /updateconfiguration switch"
  - "updateconfiguration Devenv switch"
ms.assetid: 9a1084cc-8b68-4ccc-aaea-f95939164338
caps.latest.revision: 3
ms.author: "kempb"
manager: "ghogen"
translation.priority.mt: 
  - "cs-cz"
  - "pl-pl"
  - "pt-br"
  - "tr-tr"
---
# -Updateconfiguration (devenv.exe)
Notifies [!INCLUDE[vsprvs](../dv_TeamTestALM/includes/vsprvs_md.md)] to merge the [!INCLUDE[vsprvs](../dv_TeamTestALM/includes/vsprvs_md.md)] packages on the system and check the MEF cache for any changes.  
  
## Syntax  
  
```  
devenv /updateconfiguration  
```  
  
## Remarks  
 [!INCLUDE[vsprvs](../dv_TeamTestALM/includes/vsprvs_md.md)] runs this command automatically when you install a VSIX package. You should run `devenv.exe /updateconfiguration` after patching your files so that [!INCLUDE[vsprvs](../dv_TeamTestALM/includes/vsprvs_md.md)] updates the MEF cache. This enables you to evaluate whether your fix is adequate.  
  
## Example  
 The following command line causes [!INCLUDE[vsprvs](../dv_TeamTestALM/includes/vsprvs_md.md)] to merge the [!INCLUDE[vsprvs](../dv_TeamTestALM/includes/vsprvs_md.md)] packages on the system and check the MEF cache for any changes.  
  
```  
Devenv.exe /updateconfiguration  
```  
  
## See Also  
 [Customizing Development Settings in Visual Studio](assetId:///22c4debb-4e31-47a8-8f19-16f328d7dcd3)   
 [Devenv Command Line Switches](../VS_IDE/devenv-command-line-switches.md)