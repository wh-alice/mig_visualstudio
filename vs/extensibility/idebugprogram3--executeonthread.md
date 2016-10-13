---
title: "IDebugProgram3::ExecuteOnThread"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "IDebugProgram3::ExecuteOnThread"
ms.assetid: 2f5211e3-7a3f-47bf-9595-dfc8b4895d0d
caps.latest.revision: 6
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
# IDebugProgram3::ExecuteOnThread
Executes the debugger program. The thread is returned to give the debugger information on which thread the user is viewing when executing the program.  
  
## Syntax  
  
```cpp#  
HRESULT ExecuteOnThread(  
   [in] IDebugThread2* pThread)  
```  
  
```c#  
int ExecuteOnThread(  
   IDebugThread2 pThread  
);  
```  
  
#### Parameters  
 `pThread`  
 [in] An [IDebugThread2](../extensibility/idebugthread2.md) object.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 There are three different ways that a debugger can resume execution after stopping:  
  
-   Execute: Cancel any previous step, and run until the next breakpoint and so on.  
  
-   Step: Cancel any old step, and run until the new step completes.  
  
-   Continue: Run again, and leave any old step active.  
  
 The thread passed to `ExecuteOnThread` is useful when deciding which step to cancel. If you do not know the thread, running execute cancels all steps. With knowledge of the thread, you only need to cancel the step on the active thread.  
  
## See Also  
 [Execute](../extensibility/idebugprogram2--execute.md)   
 [IDebugProgram3](../extensibility/idebugprogram3.md)