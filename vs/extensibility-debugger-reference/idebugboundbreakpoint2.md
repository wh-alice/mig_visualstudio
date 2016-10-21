---
title: "IDebugBoundBreakpoint2 | hehe"
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
  - "IDebugBoundBreakpoint2"
helpviewer_keywords: 
  - "IDebugBoundBreakpoint2 interface"
ms.assetid: df33c52e-ded2-48a0-951d-1f36c8fc922e
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
# IDebugBoundBreakpoint2
This interface represents a breakpoint that is bound to a code location.  
  
## Syntax  
  
```  
IDebugBoundBreakpoint2 : IUnknown  
```  
  
## Notes for Implementers  
 The debug engine (DE) implements this interface as part of its support for breakpoints.  
  
## Notes for Callers  
 A call to [Bind](../extensibility-debugger-reference/idebugpendingbreakpoint2--bind.md) creates this interface. Calls to [GetBreakpoint](../extensibility-debugger-reference/idebugbreakpointunboundevent2--getbreakpoint.md) and [Next](../extensibility-debugger-reference/ienumdebugboundbreakpoints2--next.md) can also obtain This interface.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugBoundBreakpoint2`.  
  
|Method|Description|  
|------------|-----------------|  
|[GetPendingBreakpoint](../extensibility-debugger-reference/idebugboundbreakpoint2--getpendingbreakpoint.md)|Gets the pending breakpoint from which the specified bound breakpoint was created.|  
|[GetState](../extensibility-debugger-reference/idebugboundbreakpoint2--getstate.md)|Gets the state of this bound breakpoint.|  
|[GetHitCount](../extensibility-debugger-reference/idebugboundbreakpoint2--gethitcount.md)|Gets the current hit count for this bound breakpoint.|  
|[GetBreakpointResolution](../extensibility-debugger-reference/idebugboundbreakpoint2--getbreakpointresolution.md)|Gets the breakpoint resolution that describes this breakpoint.|  
|[Enable](../extensibility-debugger-reference/idebugboundbreakpoint2--enable.md)|Enables or disables the breakpoint.|  
|[SetHitCount](../extensibility-debugger-reference/idebugboundbreakpoint2--sethitcount.md)|Sets the hit count for this bound breakpoint.|  
|[SetCondition](../extensibility-debugger-reference/idebugboundbreakpoint2--setcondition.md)|Sets or changes the condition associated with this bound breakpoint.|  
|[SetPassCount](../extensibility-debugger-reference/idebugboundbreakpoint2--setpasscount.md)|Sets or change the pass count associated with this bound breakpoint.|  
|[Delete](../extensibility-debugger-reference/idebugboundbreakpoint2--delete.md)|Deletes the breakpoint.|  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [GetBreakpoint](../extensibility-debugger-reference/idebugbreakpointunboundevent2--getbreakpoint.md)   
 [Next](../extensibility-debugger-reference/ienumdebugboundbreakpoints2--next.md)   
 [Bind](../extensibility-debugger-reference/idebugpendingbreakpoint2--bind.md)