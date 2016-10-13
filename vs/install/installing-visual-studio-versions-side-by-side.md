---
title: "Installing Visual Studio Versions Side-by-Side"
ms.custom: na
ms.date: "10/12/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-install"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "side-by-side installations [Visual Studio]"
  - "Help [Visual Studio], installing"
ms.assetid: 4d00f240-4910-4699-aaf3-cda6461f0c29
caps.latest.revision: 47
ms.author: "tglee"
manager: "ghogen"
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
# Installing Visual Studio Versions Side-by-Side
You can install this version of Visual Studio on a computer that already has an earlier version installed. If you encounter an installation failure, you can use the [log collection tool](http://go.microsoft.com/fwlink/?LinkId=262077) to collect information about the failures so you can debug the issues yourself.  
  
> [!NOTE]
>  We recommend that you install [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] versions in the order in which they were released. For example, install Visual Studio 2013 before you install Visual Studio 2015.  
  
 Before you install versions side by side, review the following conditions:  
  
-   If you use Visual Studio 2015 to open a solution that was created in [!INCLUDE[vs_dev12](../extensibility/includes/vs_dev12_md.md)], you can later open and modify the solution again in the older version as long as you haven't implemented any features that are specific to Visual Studio 2015.  
  
-   If you try to use Visual Studio 2015 to open a solution that was created in [!INCLUDE[vs_dev12](../extensibility/includes/vs_dev12_md.md)] or an earlier version, you might need to modify your projects and files to be compatible with Visual Studio 2015. For more information, see  [Porting, Migrating, and Upgrading Visual Studio Projects](../porting/porting--migrating--and-upgrading-visual-studio-projects.md).  
  
-   If you uninstall a version of [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] on a computer that has more than one version installed, the file associations for [!INCLUDE[vsprvs](../codequality/includes/vsprvs_md.md)] are removed for all versions. You can remap these file associations by using the **Restore File Associations** button on the **Environment**, **General** page of the [Options](../reference/general--environment--options-dialog-box.md) dialog box.  
  
-   Visual Studio doesn't automatically upgrade extensions because not all extensions are compatible. You must reinstall the extensions from the [Visual Studio Gallery](http://go.microsoft.com/fwlink/?LinkId=178891) or the software publisher.  
  
## .NET Framework Versions and Side-by-Side Installations  
  
-   Visual Basic, Visual C#, and Visual F# projects use the **Target Framework** option in the **Project Designer** to specify which version of the .NET Framework a project uses. For a C++ project, you can manually change the target framework by modifying the .vcxproj file. For more information, see [Version Compatibility](../Topic/Version%20Compatibility%20in%20the%20.NET%20Framework.md).  
  
     When you create a project, you can specify which version of the .NET Framework the project targets in the **.NET Framework** list in the **New Project** dialog box.  
  
     For language-specific information, see the appropriate topic in the following table.  
  
    |Language|Topic|  
    |--------------|-----------|  
    |[!INCLUDE[vbprvb](../codequality/includes/vbprvb_md.md)]|[Application Page, Project Designer (Visual Basic)](../reference/application-page--project-designer--visual-basic-.md)|  
    |Visual C#|[Application Page, Project Designer (C#)](../reference/application-page--project-designer--csharp-.md)|  
    |Visual F#|[Configuring Projects](../Topic/Configuring%20Projects%20\(F%23\).md)|  
    |C++|[How to: Modify the Target Framework and Platform Toolset](../Topic/How%20to:%20Modify%20the%20Target%20Framework%20and%20Platform%20Toolset.md)|  
    |[!INCLUDE[jsprjscript](../debugger/includes/jsprjscript_md.md)]|[Running a JScript Application on a Previous Version of the Common Language Runtime](http://msdn.microsoft.com/bbea51b5-ac03-4e6c-b9a6-f487ef63eda5)|  
  
## See Also  
 [Installing Visual Studio 2015](../install/installing-visual-studio-2015.md)   
 [Porting, Migrating, and Upgrading Visual Studio Projects](../porting/porting--migrating--and-upgrading-visual-studio-projects.md)   
 [Version Compatibility](../Topic/Version%20Compatibility%20in%20the%20.NET%20Framework.md)   
 [Installing Multiple Language Versions of Visual Studio](../install/installing-multiple-language-versions-of-visual-studio.md)   
 [Building C/C++ Isolated Applications and Side-by-side Assemblies](../Topic/Building%20C-C++%20Isolated%20Applications%20and%20Side-by-side%20Assemblies.md)   
 [Customizing Development Settings in Visual Studio](http://msdn.microsoft.com/22c4debb-4e31-47a8-8f19-16f328d7dcd3)