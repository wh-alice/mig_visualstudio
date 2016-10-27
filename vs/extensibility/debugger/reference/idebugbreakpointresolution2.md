---
title: "IDebugBreakpointResolution2"
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
  - "IDebugBreakpointResolution2"
helpviewer_keywords: 
  - "IDebugBreakpointRequest2 interface"
ms.assetid: 451d5bce-b9c1-48ff-beaa-2b4c3e1ceea0
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
# IDebugBreakpointResolution2
This interface represents the information that describes a bound breakpoint.  
  
## Syntax  
  
```  
IDebugBreakpointResolution2 : IUnknown  
```  
  
## Notes for Implementers  
 The debug engine (DE) implements this interface as part of its support for breakpoints. This interface provides a description of a bound breakpoint that the session debug manager uses when a user views a breakpoint's properties.  
  
## Notes for Callers  
 A call to [GetBreakpointResolution](../../../extensibility/debugger/reference/idebugboundbreakpoint2--getbreakpointresolution.md) returns this interface.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugBreakpointResolution2`.  
  
|Method|Description|  
|------------|-----------------|  
|[GetBreakpointType](../../../extensibility/debugger/reference/idebugbreakpointresolution2--getbreakpointtype.md)|Gets the type of the breakpoint represented by this resolution.|  
|[GetResolutionInfo](../../../extensibility/debugger/reference/idebugbreakpointresolution2--getresolutioninfo.md)|Gets the breakpoint resolution information that describes this breakpoint.|  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [GetBreakpointResolution](../../../extensibility/debugger/reference/idebugboundbreakpoint2--getbreakpointresolution.md)