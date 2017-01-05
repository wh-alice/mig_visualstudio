---
title: "Opening and Saving Project Items"
ms.custom: ""
ms.date: "12/07/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "projects [Visual Studio SDK], file persistence"
  - "files [Visual Studio], opening and saving"
  - "editors [Visual Studio SDK], file persistence"
ms.assetid: f71898ad-335f-4c43-a177-4da87078afd1
caps.latest.revision: 9
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
# Opening and Saving Project Items
[!INCLUDE[vs2017banner](../../code-quality/includes/vs2017banner.md)]

When you add a new project type, you must manage the opening and saving of your projects files in the [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] integrated development environment (IDE). The following topics discuss the different approaches to opening and saving files.  
  
## In This Section  
 [Displaying Files By Using the Open File Command](../../extensibility/internals/displaying-files-by-using-the-open-file-command.md)  
 Provides a step-by-step explanation of how the IDE handles the **Open File** command and the role of projects in responding to this command.  
  
 [Displaying Files By Using the Open With Command](../../extensibility/internals/displaying-files-by-using-the-open-with-command.md)  
 Provides a detailed, step-by-step explanation of how the IDE handles the **Open With** command, prompting the opening of a file that has some choice of standard editors.  
  
 [How to: Open Project-Specific Editors](../../extensibility/how-to--open-project-specific-editors.md)  
 Provides step-by-step instructions for specifying that files of a particular type in your project should be opened by using a project-specific editor.  
  
 [How to: Open Standard Editors](../../extensibility/how-to--open-standard-editors.md)  
 Provides step-by-step instructions for specifying how to enable the IDE to open a standard editor for files in your project type.  
  
 [How to: Open Editors for Open Documents](../../extensibility/how-to--open-editors-for-open-documents.md)  
 Provides step-by-step instructions to open a project-specific editor for an open file.  
  
 [Saving a Standard Document](../../extensibility/internals/saving-a-standard-document.md)  
 Provides a detailed explanation of how the IDE handles the **Save**, **Save As**, and **Save All** commands for a document opened in a standard editor.  
  
 [Saving a Custom Document](../../extensibility/internals/saving-a-custom-document.md)  
 Provides a diagram and detailed explanation of how the IDE handles the **Save**, **Save As**, and **Save All** commands for documents opened in a custom editor.  
  
 [Determining Which Editor Opens a File in a Project](../../extensibility/internals/determining-which-editor-opens-a-file-in-a-project.md)  
 Discusses the process that the IDE follows to select the appropriate editor or designer for a file.  
  
## Related Sections  
 [Creating Custom Editors and Designers](../../extensibility/creating-custom-editors-and-designers.md)  
 Lists the four types of editors that the IDE can host and gives descriptions of each editor.  
  
 [Project Types](../../extensibility/internals/project-types.md)  
 Discusses how projects control the way that code is compiled and built, how editors are opened, and how project items are formatted.