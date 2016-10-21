---
title: "BP_RESOLUTION_CODE | hehe"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "BP_RESOLUTION_CODE"
helpviewer_keywords: 
  - "BP_RESOLUTION_CODE structure"
ms.assetid: ac103ec5-771c-4667-92de-b5abb53bbb52
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
# BP_RESOLUTION_CODE
Describes the location of a code breakpoint.  
  
## Syntax  
  
```cpp#  
typedef struct _BP_RESOLUTION_CODE {   
   IDebugCodeContext2* pCodeContext;  
} BP_RESOLUTION_CODE;  
```  
  
```c#  
public struct BP_RESOLUTION_CODE {   
   public IDebugCodeContext2 pCodeContext;  
};  
```  
  
## Members  
 `pCodeContext`  
 The [IDebugCodeContext2](../extensibility-debugger-reference/idebugcodecontext2.md) object that identifies the position of the breakpoint in the code.  
  
## Remarks  
 This structure is a member of the [BP_RESOLUTION_LOCATION](../extensibility-debugger-reference/bp_resolution_location.md) structure, which is in turn a member of the [BP_RESOLUTION_INFO](../extensibility-debugger-reference/bp_resolution_info.md) structure returned by the [GetResolutionInfo](../extensibility-debugger-reference/idebugbreakpointresolution2--getresolutioninfo.md) method.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../extensibility-debugger-reference/structures-and-unions.md)   
 [BP_RESOLUTION_LOCATION](../extensibility-debugger-reference/bp_resolution_location.md)   
 [BP_RESOLUTION_INFO](../extensibility-debugger-reference/bp_resolution_info.md)   
 [GetResolutionInfo](../extensibility-debugger-reference/idebugbreakpointresolution2--getresolutioninfo.md)   
 [IDebugCodeContext2](../extensibility-debugger-reference/idebugcodecontext2.md)