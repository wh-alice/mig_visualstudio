---
title: "Providing Automation for Code"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "CodeModel object"
ms.assetid: 21cb3e63-f25c-404b-bc1d-a32ad0fdd4d5
caps.latest.revision: 13
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
# Providing Automation for Code
Creating an automation model for your code is not required. The Environment SDK does not provide a sample for doing so. For insight into code models, see the \<xref:EnvDTE.CodeModel> object.  
  
 To implement a code model, you must implement any interfaces that are determined by your internal data structure. The objects must be derived from the `IDispatch` class.  
  
 The objects that you extend, \<xref:EnvDTE.CodeModel> and \<xref:EnvDTE.FileCodeModel>, are available from the \<xref:EnvDTE.Project> object, and look like the following:  
  
 \<xref:EnvDTE.Project.CodeModel*>  
  
 \<xref:EnvDTE.ProjectItem.FileCodeModel*>  
  
 You can elect to implement just the `CodeModel` or the `FileCodeModel` interface in the object you return from your `Project` and \<xref:EnvDTE.ProjectItem> objects. Provide any functionality from this interface that is appropriate for your project system.  
  
 If you want to add features, such as methods or properties, that are not available from the standard `CodeModel` and `FileCodeModel` interfaces, create your own interface that inherits from the standard. Be sure to document it with your project system so end users will know to look for it. You return the standard interface, but the user can call the `QueryInterface` method or cast to your interface if it is known to exist.  
  
## See Also  
 [Automation Model Overview](../extensibility/automation-model-overview.md)