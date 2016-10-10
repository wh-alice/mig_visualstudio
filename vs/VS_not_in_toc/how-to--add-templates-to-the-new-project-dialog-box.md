---
title: "How to: Add Templates to the New Project Dialog Box"
ms.custom: na
ms.date: "10/10/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "dialog boxes, adding templates to project"
  - "projects [Visual Studio SDK], adding templates to dialog box"
  - "templates [Visual Studio], adding to project dialog box"
ms.assetid: fd044681-e666-410d-815c-33db923ed888
caps.latest.revision: 26
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
# How to: Add Templates to the New Project Dialog Box
A number of predefined project templates are installed during [!INCLUDE[vsprvs](../dv_TeamTestALM/includes/vsprvs_md.md)] installation. For a complete list of predefined project templates, see [NIB Creating Projects from Templates](assetId:///7c36d86a-6b79-4480-8228-0f925f1204b2). In addition to default project templates you can create custom or subtype-specific project templates. For example, the **Smart Device** subtype provides its own templates for [!INCLUDE[csprcs](../VS_debugger/includes/csprcs_md.md)] and [!INCLUDE[vbprvb](../VS_debugger/includes/vbprvb_md.md)] projects. For instructions on how to create a custom template, see [How to: Create Project Templates](../VS_IDE/how-to--create-project-templates.md).  
  
## Adding a Template to the New Project Dialog Box  
  
#### To add a template to the New Project dialog box  
  
1.  Create a template, including the MyTemplate.vstemplate file.  
  
2.  Select the files in your template (including the .vstemplate file), right-click them, click **Send To**, and then click **Compressed (zipped) Folder**. The files that you previously extracted are compressed into a .zip file.  
  
 Put the .zip template file in **%USERPROFILE%\Documents\Visual Studio 2015\Templates\ProjectTemplates**.  
  
## See Also  
 [Project Subtypes](d235b47b-cf11-4d47-a63f-e33d9d16105d2044a030-0795-4940-bd65-a6e44de98a0f)   
 [NIB: Visual Studio Templates](assetId:///141fccaa-d68f-4155-822b-27f35dd94041)   
 [Contributing to the Add New Item Dialog Box](../Topic/Contributing%20to%20the%20Add%20New%20Item%20Dialog%20Box.md)