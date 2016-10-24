---
title: "XslTransformation Task"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
  - "CSharp"
  - "C++"
  - "jsharp"
helpviewer_keywords: 
  - "MSBuild, XslTransformation task"
  - "XslTransformation task [MSBuild]"
ms.assetid: 6f3a7d81-3ae3-4703-9a06-870b32b69d80
caps.latest.revision: 4
ms.author: "kempb"
manager: "ghogen"
translation.priority.ht: 
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
# XslTransformation Task
Transforms an XML input by using an XSLT or compiled XSLT and outputs to an output device or a file.  
  
## Parameters  
 The following table describes the parameters of the `XslTransformation` task.  
  
|Parameter|Description|  
|---------------|-----------------|  
|`OutputPaths`|Required <xref:Microsoft.Build.Framework.ITaskItem>`[]` parameter.<br /><br /> Specifies the output files for the XML transformation.|  
|`Parameters`|Optional `String` parameter.<br /><br /> Specifies the parameters to the XSLT Input document.|  
|`XmlContent`|Optional `String` parameter.<br /><br /> Specifies the XML input as a string.|  
|`XmlInputPaths`|Optional <xref:Microsoft.Build.Framework.ITaskItem>`[]` parameter.<br /><br /> Specifies the XML input files.|  
|`XslCompiledDllPath`|Optional <xref:Microsoft.Build.Framework.ITaskItem> parameter.<br /><br /> Specifies the compiled XSLT.|  
|`XslContent`|Optional `String` parameter.<br /><br /> Specifies the XSLT input as a string.|  
|`XslInputPath`|Optional <xref:Microsoft.Build.Framework.ITaskItem> parameter.<br /><br /> Specifies the XSLT input file.|  
  
## Remarks  
 In addition to having the parameters that are listed in the table, this task inherits parameters from the <xref:Microsoft.Build.Tasks.TaskExtension> class, which itself inherits from the <xref:Microsoft.Build.Utilities.Task> class. For a list of these additional parameters and their descriptions, see [TaskExtension Base Class](../reference/taskextension-base-class.md).  
  
## See Also  
 [Tasks](../reference/msbuild-tasks.md)   
 [Task Reference](../reference/msbuild-task-reference.md)