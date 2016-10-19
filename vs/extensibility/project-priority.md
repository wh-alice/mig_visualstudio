---
title: "Project Priority"
ms.custom: ""
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "projects [Visual Studio SDK], opening items"
ms.assetid: 9f707592-2fb6-4f75-9269-f6d4700a998e
caps.latest.revision: 11
ms.author: "gregvanl"
manager: "ghogen"
translation.priority.mt: 
  - "cs-cz"
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "pl-pl"
  - "pt-br"
  - "ru-ru"
  - "tr-tr"
  - "zh-cn"
  - "zh-tw"
---
# Project Priority
A project item usually is a member of only one project in the solution. Therefore, the IDE can easily determine which project is used to open the item. However, if an item is a member of more than one project, the IDE uses a priority scheme to determine the best project for opening the item.  
  
 The following list shows the project priority scheme:  
  
-   The IDE calls the <xref:Microsoft.VisualStudio.Shell.Interop.IVsProject2.IsDocumentInProject*> method for each project in the solution to determine whether the document is a member of that project.  
  
-   If the document is a member of the project, the project responds with a priority that the project assigns according to its handling of that document. For example, a language project responds with a high priority for its language source files but responds with a lower priority for an unrecognized file type that is not used as part of its build process.  
  
-   Projects that provide custom, project-specific editors or designers for a document also receive a high priority.  
  
-   The <xref:Microsoft.VisualStudio.Shell.Interop.VSDOCUMENTPRIORITY> enumeration provides the document priority values.  
  
-   The project that specifies the highest priority is given the context to open the document. If two projects return equal priority values, the active project is preferred. If no project in the solution responds that it can open the document, the IDE puts the document in the Miscellaneous Files project. For more information, see [Miscellaneous Files Project](../extensibility/miscellaneous-files-project.md).  
  
## See Also  
 [Miscellaneous Files Project](../extensibility/miscellaneous-files-project.md)   
 [How to: Open Editors for Open Documents](../extensibility/how-to--open-editors-for-open-documents.md)   
 [Adding Project and Project Item Templates](../extensibility/adding-project-and-project-item-templates.md)