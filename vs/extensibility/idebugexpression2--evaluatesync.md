---
title: "IDebugExpression2::EvaluateSync"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "IDebugExpression2::EvaluateSync"
helpviewer_keywords: 
  - "IDebugExpression2::EvaluateSync"
ms.assetid: 88964915-dce3-4005-b4f3-9f37415e41e4
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
# IDebugExpression2::EvaluateSync
This method evaluates the expression synchronously.  
  
## Syntax  
  
```cpp#  
HRESULT EvaluateSync(   
   EVALFLAGS             dwFlags,  
   DWORD                 dwTimeout,  
   IDebugEventCallback2* pExprCallback,  
   IDebugProperty2**     ppResult  
);  
```  
  
```c#  
int EvaluateSync(  
   enum_EVALFLAGS       dwFlags,   
   uint                 dwTimeout,   
   IDebugEventCallback2 pExprCallback,   
   out IDebugProperty2  ppResult  
);  
```  
  
#### Parameters  
 `dwFlags`  
 [in] A combination of flags from the [EVALFLAGS](../extensibility/evalflags.md) enumeration that control expression evaluation.  
  
 `dwTimeout`  
 [in] Maximum time, in milliseconds, to wait before returning from this method. Use `INFINITE` to wait indefinitely.  
  
 `pExprCallback`  
 [in]This parameter is always a null value.  
  
 `ppResult`  
 [out] Returns the [IDebugProperty2](../extensibility/idebugproperty2.md) object that contains the result of the expression evaluation.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise returns an error code. Some typical error codes are:  
  
|Error|Description|  
|-----------|-----------------|  
|E_EVALUATE_BUSY_WITH_EVALUATION|Another expression is currently being evaluated, and simultaneous expression evaluation is not supported.|  
|E_EVALUATE_TIMEOUT|Evaluation timed out.|  
  
## Remarks  
 For synchronous evaluation, it is not necessary to send an event back to Visual Studio upon completion of the evaluation.  
  
## Example  
 The following example shows how to implement this method for a simple `CExpression` object that implements the [IDebugExpression2](../extensibility/idebugexpression2.md) interface.  
  
```cpp#  
HRESULT CExpression::EvaluateSync(EVALFLAGS dwFlags,  
                                  DWORD dwTimeout,  
                                  IDebugEventCallback2* pExprCallback,  
                                  IDebugProperty2** ppResult)  
{  
    // Set the aborted state to FALSE.    
    m_bAborted = FALSE;    
    // Delegate the evaluation to EvalExpression.    
    return EvalExpression(TRUE, ppResult);    
}  
  
HRESULT CExpression::EvalExpression(BOOL bSynchronous,  
                                    IDebugProperty2** ppResult)  
{  
    HRESULT hr;  
  
    // Get the value of an environment variable.  
    PCSTR pszVal = m_pEnvBlock->GetEnv(m_pszVarName);  
    // Create and initialize a CEnvVar object with the retrieved value.  
    // CEnvVar implements the IDebugProperty2 interface.  
    CComObject<CEnvVar> *pEnvVar;  
    CComObject<CEnvVar>::CreateInstance(&pEnvVar);  
    pEnvVar->Init(m_pszVarName, pszVal, m_pDoc);  
  
    if (pszVal) {  
        // Check for synchronous evaluation.  
        if (bSynchronous) {  
            // Set and AddRef the result, IDebugProperty2 interface.  
            *ppResult = pEnvVar;  
            (*ppResult)->AddRef();  
            hr = S_OK;  
        } else {  
            //For asynchronous evaluation, send an evaluation complete event.  
            CExprEvalEvent *pExprEvent = new CExprEvalEvent(this, pEnvVar);  
            pExprEvent->SendEvent(m_pExprCallback, NULL, NULL, NULL);  
        }  
    } else {  
        // If a valid value is not retrieved, return E_FAIL.  
        hr = E_FAIL;  
    }  
    return hr;  
}  
```  
  
## See Also  
 [IDebugExpression2](../extensibility/idebugexpression2.md)   
 [EVALFLAGS](../extensibility/evalflags.md)   
 [IDebugEventCallback2](../extensibility/idebugeventcallback2.md)   
 [IDebugProperty2](../extensibility/idebugproperty2.md)