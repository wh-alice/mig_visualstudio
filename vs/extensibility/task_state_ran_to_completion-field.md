---
title: "TASK_STATE_RAN_TO_COMPLETION Field"
ms.custom: na
ms.date: "10/13/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "TASK_STATE_RAN_TO_COMPLETION field, Task class [.NET Framework debug engines]"
ms.assetid: 0f4830af-fe0c-4141-b768-817f4e426b8c
caps.latest.revision: 8
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
# TASK_STATE_RAN_TO_COMPLETION Field
The task completed execution successfully.  
  
 **Namespace:** \<xref:System.Threading.Tasks?displayProperty=fullName>  
  
 **Assembly:** mscorlib (in mscorlib.dll)  
  
 Because you cannot access this internal member from the .NET Framework, the following syntax is provided in Common Intermediate Language (CIL).  
  
## Syntax  
  
```  
.field static assembly literal int32 TASK_STATE_RAN_TO_COMPLETION = int32(0x02000000)  
```  
  
## Remarks  
 If the [m_stateFlags](../extensibility/m_stateflags-field.md) field contains this value, the \<xref:System.Threading.Tasks.Task.Status*> property returns \<xref:System.Threading.Tasks.TaskStatus?displayProperty=fullName>.  
  
## See Also  
 [Task Class](../extensibility/task-class---internal-members.md)