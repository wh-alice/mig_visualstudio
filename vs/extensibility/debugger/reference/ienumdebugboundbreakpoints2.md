---
title: "IEnumDebugBoundBreakpoints2"
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
  - "IEnumDebugBoundBreakpoints2"
helpviewer_keywords: 
  - "IEnumDebugBoundBreakpoints2"
ms.assetid: ea03e7e1-28d6-40b7-8097-bbb61d3b7caa
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
# IEnumDebugBoundBreakpoints2
[!INCLUDE[vs2017banner](../../../code-quality/includes/vs2017banner.md)]

This interface enumerates the bound breakpoints associated with a pending breakpoint or breakpoint bound event.  
  
## Syntax  
  
```  
IEnumDebugBoundBreakpoints2 : IUnknown  
```  
  
## Notes for Implementers  
 The debug engine (DE) implements this interface as part of its support for breakpoints. This interface must be implemented if breakpoints are supported.  
  
## Notes for Callers  
 Visual Studio calls:  
  
-   [EnumBreakpoints](../../../extensibility/debugger/reference/idebugbreakpointevent2--enumbreakpoints.md) to obtain this interface representing a list of all breakpoints that were triggered.  
  
-   [EnumBoundBreakpoints](../../../extensibility/debugger/reference/idebugbreakpointboundevent2--enumboundbreakpoints.md) to obtain this interface representing a list of all breakpoints that were bound.  
  
-   [EnumBoundBreakpoints](../../../extensibility/debugger/reference/idebugpendingbreakpoint2--enumboundbreakpoints.md) to obtain this interface representing a list of all breakpoints bound to that pending breakpoint.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IEnumDebugBoundBreakpoints2`.  
  
|Method|Description|  
|------------|-----------------|  
|[Next](../../../extensibility/debugger/reference/ienumdebugboundbreakpoints2--next.md)|Retrieves a specified number of bound breakpoints in an enumeration sequence.|  
|[Skip](../../../extensibility/debugger/reference/ienumdebugboundbreakpoints2--skip.md)|Skips a specified number of bound breakpoints in an enumeration sequence.|  
|[Reset](../../../extensibility/debugger/reference/ienumdebugboundbreakpoints2--reset.md)|Resets an enumeration sequence to the beginning.|  
|[Clone](../../../extensibility/debugger/reference/ienumdebugboundbreakpoints2--clone.md)|Creates an enumerator that contains the same enumeration state as the current enumerator.|  
|[GetCount](../../../extensibility/debugger/reference/ienumdebugboundbreakpoints2--getcount.md)|Gets the number of bound breakpoints in an enumerator.|  
  
## Remarks  
 Visual Studio uses the bound breakpoints represented by this interface to update the display of breakpoints in the IDE.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../../../extensibility/debugger/reference/core-interfaces.md)   
 [EnumBoundBreakpoints](../../../extensibility/debugger/reference/idebugbreakpointboundevent2--enumboundbreakpoints.md)   
 [EnumBoundBreakpoints](../../../extensibility/debugger/reference/idebugpendingbreakpoint2--enumboundbreakpoints.md)   
 [EnumBoundBreakpoints](../../../extensibility/debugger/reference/idebugpendingbreakpoint2--enumboundbreakpoints.md)