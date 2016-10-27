---
title: "IDebugPendingBreakpoint2::GetState"
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
  - "IDebugPendingBreakpoint2::GetState"
helpviewer_keywords: 
  - "GetState method"
  - "IDebugPendingBreakpoint2::GetState method"
ms.assetid: e88d543f-2e83-4ba7-86ca-f874e39955ff
caps.latest.revision: 10
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
# IDebugPendingBreakpoint2::GetState
Gets the state of the pending breakpoint.  
  
## Syntax  
  
```cpp#  
HRESULT GetState(   
   PENDING_BP_STATE_INFO* pState  
);  
```  
  
```c#  
int GetState(   
   PENDING_BP_STATE_INFO[] pState  
);  
```  
  
#### Parameters  
 `pState`  
 [in, out] A [PENDING_BP_STATE_INFO](../../../extensibility/debugger/reference/pending_bp_state_info.md) structure that is filled in with a description of this pending breakpoint.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugPendingBreakpoint2](../../../extensibility/debugger/reference/idebugpendingbreakpoint2.md)   
 [PENDING_BP_STATE_INFO](../../../extensibility/debugger/reference/pending_bp_state_info.md)