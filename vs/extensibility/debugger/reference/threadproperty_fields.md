---
title: "THREADPROPERTY_FIELDS"
ms.custom: ""
ms.date: "12/07/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "THREADPROPERTY_FIELDS"
helpviewer_keywords: 
  - "THREADPROPERTY_FIELDS enumeration"
ms.assetid: 5b88acb9-03ea-4c29-a788-f0087dccbe23
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
# THREADPROPERTY_FIELDS
[!INCLUDE[vs2017banner](../../../code-quality/includes/vs2017banner.md)]

Specifies what information about a thread is to be retrieved.  
  
## Syntax  
  
```cpp#  
enum enum_THREADPROPERTY_FIELDS {   
   TPF_ID           = 0x0001,  
   TPF_SUSPENDCOUNT = 0x0002,  
   TPF_STATE        = 0x0004,  
   TPF_PRIORITY     = 0x0008,  
   TPF_NAME         = 0x0010,  
   TPF_LOCATION     = 0x0020,  
   TPF_ALLFIELDS    = 0xffffffff  
};  
typedef DWORD THREADPROPERTY_FIELDS;  
```  
  
```c#  
public enum enum_THREADPROPERTY_FIELDS {   
   TPF_ID           = 0x0001,  
   TPF_SUSPENDCOUNT = 0x0002,  
   TPF_STATE        = 0x0004,  
   TPF_PRIORITY     = 0x0008,  
   TPF_NAME         = 0x0010,  
   TPF_LOCATION     = 0x0020,  
   TPF_ALLFIELDS    = 0xffffffff  
};  
```  
  
## Members  
 TPF_ID  
 Initialize/use the `dwThreadId` field of the [THREADPROPERTIES](../../../extensibility/debugger/reference/threadproperties.md) structure.  
  
 TPF_SUSPENDCOUNT  
 Initialize/use the `dwSuspendCount` field of the `THREADPROPERTIE`S structure.  
  
 TPF_STATE  
 Initialize/use the `dwThreadState` field of the `THREADPROPERTIE`S structure.  
  
 TPF_PRIORITY  
 Initialize/use the `bstrPriority` field of the `THREADPROPERTIE`S structure.  
  
 TPF_NAME  
 Initialize/use the `bstrName` field of the `THREADPROPERTIE`S structure.  
  
 TPF_LOCATION  
 Initialize/use the `bstrLocation` field of the `THREADPROPERTIE`S structure.  
  
 TPF_ALLFIELDS  
 Specifies all fields.  
  
## Remarks  
 These values are passed as an argument to the [GetThreadProperties](../../../extensibility/debugger/reference/idebugthread2--getthreadproperties.md) method to indicate which fields of the [THREADPROPERTIES](../../../extensibility/debugger/reference/threadproperties.md) structure are to be initialized.  
  
 These values are also used in `dwFields` member of the `THREADPROPERTIES` structure to indicate which fields are used and valid.  
  
 These flags may be combined with a bitwise `OR`.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations](../../../extensibility/debugger/reference/enumerations--visual-studio-debugging-.md)   
 [THREADPROPERTIES](../../../extensibility/debugger/reference/threadproperties.md)   
 [GetThreadProperties](../../../extensibility/debugger/reference/idebugthread2--getthreadproperties.md)