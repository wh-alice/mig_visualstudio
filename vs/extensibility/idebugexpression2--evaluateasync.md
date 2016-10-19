---
title: "IDebugExpression2::EvaluateAsync"
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
  - "IDebugExpression2::EvaluateAsync"
helpviewer_keywords: 
  - "IDebugExpression2::EvaluateAsync"
ms.assetid: 848fe6cb-0759-42f2-890b-d2b551c527d6
caps.latest.revision: 15
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
# IDebugExpression2::EvaluateAsync
This method evaluates the expression asynchronously.  
  
## Syntax  
  
```cpp#  
HRESULT EvaluateAsync (   
   EVALFLAGS             dwFlags,  
   IDebugEventCallback2* pExprCallback  
);  
```  
  
```c#  
int EvaluateAsync(  
   enum_EVALFLAGS       dwFlags,   
   IDebugEventCallback2 pExprCallback  
);  
```  
  
#### Parameters  
 `dwFlags`  
 [in] A combination of flags from the [EVALFLAGS](../extensibility/evalflags.md) enumeration that control expression evaluation.  
  
 `pExprCallback`  
 [in] This parameter is always a null value.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise returns an error code. A typical error code is:  
  
|Error|Description|  
|-----------|-----------------|  
|E_EVALUATE_BUSY_WITH_EVALUATION|Another expression is currently being evaluated, and simultaneous expression evaluation is not supported.|  
  
## Remarks  
 This method should return immediately after it has started the expression evaluation. When the expression is successfully evaluated, an [IDebugExpressionEvaluationCompleteEvent2](../extensibility/idebugexpressionevaluationcompleteevent2.md) must be sent to the [IDebugEventCallback2](../extensibility/idebugeventcallback2.md) event callback as supplied through [Attach](../extensibility/idebugprogram2--attach.md) or [Attach](../extensibility/idebugengine2--attach.md).  
  
## Example  
 The following example shows how to implement this method for a simple `CExpression` object that implements the [IDebugExpression2](../extensibility/idebugexpression2.md) interface.  
  
```cpp#  
HRESULT CExpression::EvaluateAsync(EVALFLAGS dwFlags,  
                                   IDebugEventCallback2* pExprCallback)  
{  
    // Set the aborted state to FALSE  
    // in case the user tries to redo the evaluation after aborting.  
    m_bAborted = FALSE;  
    // Post the WM_EVAL_EXPR message in the message queue of the current thread.  
    // This starts the expression evaluation on a background thread.  
    PostThreadMessage(GetCurrentThreadId(), WM_EVAL_EXPR, 0, (LPARAM) this);  
    return S_OK;  
}  
```  
  
## See Also  
 [IDebugExpression2](../extensibility/idebugexpression2.md)   
 [IDebugExpressionEvaluationCompleteEvent2](../extensibility/idebugexpressionevaluationcompleteevent2.md)   
 [EVALFLAGS](../extensibility/evalflags.md)   
 [IDebugEventCallback2](../extensibility/idebugeventcallback2.md)