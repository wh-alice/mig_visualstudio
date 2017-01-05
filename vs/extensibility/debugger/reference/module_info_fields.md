---
title: "MODULE_INFO_FIELDS"
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
  - "MODULE_INFO_FIELDS"
helpviewer_keywords: 
  - "MODULE_INFO_FIELDS enumeration"
ms.assetid: 8bed85f4-235f-4192-b58f-5fad7a4d7a78
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
# MODULE_INFO_FIELDS
[!INCLUDE[vs2017banner](../../../code-quality/includes/vs2017banner.md)]

Specifies the flags for the debug module information.  
  
## Syntax  
  
```cpp#  
enum enum_MODULE_INFO_FIELDS {   
   MIF_NONE              = 0x0000,  
   MIF_NAME              = 0x0001,  
   MIF_URL               = 0x0002,  
   MIF_VERSION           = 0x0004,  
   MIF_DEBUGMESSAGE      = 0x0008,  
   MIF_LOADADDRESS       = 0x0010,  
   MIF_PREFFEREDADDRESS  = 0x0020,  
   MIF_SIZE              = 0x0040,  
   MIF_LOADORDER         = 0x0080,  
   MIF_TIMESTAMP         = 0x0100,  
   MIF_URLSYMBOLLOCATION = 0x0200,  
   MIF_FLAGS             = 0x0400,  
   MIF_ALLFIELDS         = 0x07ff  
};  
typedef DWORD MODULE_INFO_FIELDS;  
```  
  
```c#  
public enum enum_MODULE_INFO_FIELDS {   
   MIF_NONE              = 0x0000,  
   MIF_NAME              = 0x0001,  
   MIF_URL               = 0x0002,  
   MIF_VERSION           = 0x0004,  
   MIF_DEBUGMESSAGE      = 0x0008,  
   MIF_LOADADDRESS       = 0x0010,  
   MIF_PREFFEREDADDRESS  = 0x0020,  
   MIF_SIZE              = 0x0040,  
   MIF_LOADORDER         = 0x0080,  
   MIF_TIMESTAMP         = 0x0100,  
   MIF_URLSYMBOLLOCATION = 0x0200,  
   MIF_FLAGS             = 0x0400,  
   MIF_ALLFIELDS         = 0x07ff  
};  
```  
  
## Members  
 MIF_NONE  
 Initialize/use none of the fields in the structure.  
  
 MIF_NAME  
 Initialize/use the `m_bstrName` field in the [MODULE_INFO](../../../extensibility/debugger/reference/module_info.md) structure.  
  
 MIF_URL  
 Initialize/use the `m_bstrUrl` field in the `MODULE_INFO` structure.  
  
 MIF_VERSION  
 Initialize/use the `m_bstrVersion` field in the `MODULE_INFO` structure.  
  
 MIF_DEBUGMESSAGE  
 Initialize/use the `m_bstrDebugMessage` field in the `MODULE_INFO` structure.  
  
 MIF_LOADADDRESS  
 Initialize/use the `m_addrLoadAddress` field in the `MODULE_INFO` structure.  
  
 MIF_PREFFEREDADDRESS  
 Initialize/use the `m_addrPreferredLoadAddress` field in the `MODULE_INFO` structure.  
  
 MIF_SIZE  
 Initialize/use the `m_dwSize` field in the `MODULE_INFO` structure.  
  
 MIF_LOADORDER  
 Initialize/use the `m_dwLoadOrder` field in the `MODULE_INFO` structure.  
  
 MIF_TIMESTAMP  
 Initialize/use the `m_TimeStamp` field in the `MODULE_INFO` structure.  
  
 MIF_URLSYMBOLLOCATION  
 Initialize/use the `m_bstrUrlSymbolLocation` field in the `MODULE_INFO` structure.  
  
 MIF_FLAGS  
 Initialize/use the `m_dwModuleFlags` field in the `MODULE_INFO` structure.  
  
 MIF_ALLFIELDS  
 Initialize/use all of the fields in the `MODULE_INFO` structure.  
  
## Remarks  
 These values are passed as an argument to the [GetInfo](../../../extensibility/debugger/reference/idebugmodule2--getinfo.md) method to indicate which fields of the [MODULE_INFO](../../../extensibility/debugger/reference/module_info.md) structure are to be initialized.  
  
 These values are also used in the `MODULE_INFO` structure to indicate which fields are used and valid.  
  
 These flags may be combined with a bitwise `OR`.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Enumerations](../../../extensibility/debugger/reference/enumerations--visual-studio-debugging-.md)   
 [MODULE_INFO](../../../extensibility/debugger/reference/module_info.md)   
 [GetInfo](../../../extensibility/debugger/reference/idebugmodule2--getinfo.md)