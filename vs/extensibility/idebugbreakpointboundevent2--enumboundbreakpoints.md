---
title: "IDebugBreakpointBoundEvent2::EnumBoundBreakpoints"
ms.custom: ""
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "IDebugBreakpointBoundEvent2::EnumBoundBreakpoints"
helpviewer_keywords: 
  - "IDebugBreakpointBoundEvent2::EnumBoundBreakpoints"
ms.assetid: 1f588feb-522e-488d-be92-7bc19b9e3688
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
# IDebugBreakpointBoundEvent2::EnumBoundBreakpoints
Creates an enumerator of breakpoints that were bound on this event.  
  
## Syntax  
  
```cpp#  
HRESULT EnumBoundBreakpoints(   
   IEnumDebugBoundBreakpoints2** ppEnum  
);  
```  
  
```c#  
int EnumBoundBreakpoints(   
   out IEnumDebugBoundBreakpoints2 ppEnum  
);  
```  
  
#### Parameters  
 `ppEnum`  
 [out] Returns an [IEnumDebugBoundBreakpoints2](../extensibility/ienumdebugboundbreakpoints2.md) object that enumerates all the breakpoints bound from this event.  
  
## Return Value  
 If successful, returns `S_OK`. Returns `S_FALSE` if there are no bound breakpoints; otherwise, returns an error code.  
  
## Remarks  
 The list of bound breakpoints is for those bound to this event and might not be the entire list of breakpoints bound from a pending breakpoint. To get a list of all breakpoints bound to a pending breakpoint, call the [GetPendingBreakpoint](../extensibility/idebugbreakpointboundevent2--getpendingbreakpoint.md) method to get the associated [IDebugPendingBreakpoint2](../extensibility/idebugpendingbreakpoint2.md) object and then call the [EnumBoundBreakpoints](../extensibility/idebugpendingbreakpoint2--enumboundbreakpoints.md) method to get an [IEnumDebugBoundBreakpoints2](../extensibility/ienumdebugboundbreakpoints2.md) object which contains all the bound breakpoints for the pending breakpoint.  
  
## Example  
 The following example shows how to implement this method for a **CBreakpointSetDebugEventBase** object that exposes the [IDebugBreakpointBoundEvent2](../extensibility/idebugbreakpointboundevent2.md) interface.  
  
```cpp#  
STDMETHODIMP CBreakpointSetDebugEventBase::EnumBoundBreakpoints(  
    IEnumDebugBoundBreakpoints2 **ppEnum)  
{  
    HRESULT hRes = E_FAIL;  
  
    if ( ppEnum )  
    {  
        if ( m_pEnumBound )  
        {  
            hRes = m_pEnumBound->Clone(ppEnum);  
  
            if ( EVAL(S_OK == hRes) )  
                (*ppEnum)->Reset();  
        }  
        else  
            hRes = E_FAIL;  
    }  
    else  
        hRes = E_INVALIDARG;  
  
    return ( hRes );  
}  
```  
  
## See Also  
 [IDebugBreakpointBoundEvent2](../extensibility/idebugbreakpointboundevent2.md)   
 [IEnumDebugBoundBreakpoints2](../extensibility/ienumdebugboundbreakpoints2.md)   
 [GetPendingBreakpoint](../extensibility/idebugbreakpointboundevent2--getpendingbreakpoint.md)   
 [IDebugPendingBreakpoint2](../extensibility/idebugpendingbreakpoint2.md)   
 [EnumBoundBreakpoints](../extensibility/idebugpendingbreakpoint2--enumboundbreakpoints.md)