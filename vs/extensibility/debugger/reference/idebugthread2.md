---
title: "IDebugThread2"
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
  - "IDebugThread2"
helpviewer_keywords: 
  - "IDebugThread2 interface"
ms.assetid: 221b4b1b-4a26-466e-bc29-5eff800fab13
caps.latest.revision: 12
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
# IDebugThread2
[!INCLUDE[vs2017banner](../../../code-quality/includes/vs2017banner.md)]

This interface represents a thread running in a program.  
  
## Syntax  
  
```  
IDebugThread2 : IUnknown  
```  
  
## Notes for Implementers  
 The debug engine (DE) implements this interface to represent a thread of execution in a single program.  
  
## Notes for Callers  
 Call [GetThread](../../../extensibility/debugger/reference/idebugstackframe2--getthread.md) to obtain this interface representing the currently active thread.  
  
 This interface is also used in creating a breakpoint request (see [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp_request_info.md)).  
  
 This interface is also returned when resolving a bound or error breakpoint (see [BP_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp_resolution_info.md) and [BP_ERROR_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp_error_resolution_info.md)).  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugThread2`.  
  
|Method|Description|  
|------------|-----------------|  
|[EnumFrameInfo](../../../extensibility/debugger/reference/idebugthread2--enumframeinfo.md)|Retrieves a list of the stack frames for this thread.|  
|[GetName](../../../extensibility/debugger/reference/idebugthread2--getname.md)|Gets the name of the thread.|  
|[SetThreadName](../../../extensibility/debugger/reference/idebugthread2--setthreadname.md)|Sets the name of the thread.|  
|[GetProgram](../../../extensibility/debugger/reference/idebugthread2--getprogram.md)|Gets the program in which a thread is running.|  
|[CanSetNextStatement](../../../extensibility/debugger/reference/idebugthread2--cansetnextstatement.md)|Determines whether the next statement can be set to the given stack frame and code context.|  
|[SetNextStatement](../../../extensibility/debugger/reference/idebugthread2--setnextstatement.md)|Sets the next statement to the given stack frame and code context.|  
|[GetThreadId](../../../extensibility/debugger/reference/idebugthread2--getthreadid.md)|Gets the system thread identifier.|  
|[Suspend](../../../extensibility/debugger/reference/idebugthread2--suspend.md)|Suspends a thread.|  
|[Resume](../../../extensibility/debugger/reference/idebugthread2--resume.md)|Resumes a thread.|  
|[GetThreadProperties](../../../extensibility/debugger/reference/idebugthread2--getthreadproperties.md)|Gets properties that describe a thread.|  
|[GetLogicalThread](../../../extensibility/debugger/reference/idebugthread2--getlogicalthread.md)|Gets the logical thread associated with this physical thread.|  
  
## Remarks  
 Because a single physical thread can run in multiple programs, more than one `IDebugThread2` from more than one program can represent the same physical thread.  
  
 When a breakpoint or exception occurs, an event is sent by calling [Event](../../../extensibility/debugger/reference/idebugeventcallback2--event.md). One of the arguments to this method is an `IDebugThread2` interface representing the current thread. [EnumFrameInfo](../../../extensibility/debugger/reference/idebugthread2--enumframeinfo.md) is used to obtain the [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md) interface for the current stack frame.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../../../extensibility/debugger/reference/core-interfaces.md)   
 [Event](../../../extensibility/debugger/reference/idebugeventcallback2--event.md)   
 [GetThread](../../../extensibility/debugger/reference/idebugstackframe2--getthread.md)   
 [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp_request_info.md)   
 [BP_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp_resolution_info.md)   
 [BP_ERROR_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp_error_resolution_info.md)