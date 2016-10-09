---
title: "Determining the Default Namespace of a Project"
ms.custom: na
ms.date: "10/01/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "custom tools, computing default namespace"
ms.assetid: 6d890676-7016-458c-8a6a-95cc0a068612
caps.latest.revision: 13
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
# Determining the Default Namespace of a Project
For [!INCLUDE[vbprvb](../VS_debugger/includes/vbprvb_md.md)], if the `CustomToolNamespace` property is set on the input file, then the value of `CustomToolNamespace` becomes the value of the default namespace parameter passed to the \<xref:Microsoft.VisualStudio.Shell.Interop.IVsSingleFileGenerator.Generate*> method. Otherwise, the `wszDefaultNamespace` parameter passed to `Generate` is always equal to the root namespace. For more information on namespaces, see [Namespace Keywords](../Topic/Namespace%20Keywords%20\(C%23%20Reference\).md).  
  
 [!INCLUDE[csprcs](../VS_debugger/includes/csprcs_md.md)] uses folder-based namespaces. That is, the namespace consists of the root namespace, plus names of any folders containing the custom tool. Each folder name is converted into a valid identifier, and periods separate all names. For example, if the input file is FolderA\FolderB\FolderC\MyInput.txt, and the root namespace is CL9, then the computed default namespace would be **CL9.FolderA.FolderB.FolderC**.  
  
 An exception to this rule occurs when the hierarchy chain contains a Web reference folder. For example, if:  
  
-   FolderC were a Web reference folder, the namespace would be **CL9.FolderC**.  
  
-   FolderB were a Web reference folder, the namespace would be **CL9.FolderB.FolderC**.  
  
 That is, the namespace uses the following format:  
  
```  
rootNamespace.webReferenceFolder.containedFolder.containedFolder ...  
```  
  
## See Also  
 [Implementing Single-File Generators](../Topic/Implementing%20Single-File%20Generators.md)   
 [Registering Single File Generators](../Topic/Registering%20Single%20File%20Generators.md)   
 [Exposing Types to Visual Designers](../Topic/Exposing%20Types%20to%20Visual%20Designers.md)