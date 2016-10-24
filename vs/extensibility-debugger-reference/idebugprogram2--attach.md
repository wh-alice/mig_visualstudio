---
title: "IDebugProgram2::Attach | testtitle"
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
  - "IDebugProgram2::Attach"
helpviewer_keywords: 
  - "IDebugProgram2::Attach"
ms.assetid: de069fbf-a565-4905-b102-f5658c55aacd
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
# IDebugProgram2::Attach
Attaches to the program.  
  
## Syntax  
  
```cpp#  
HRESULT Attach(   
   IDebugEventCallback2* pCallback  
);  
```  
  
```c#  
int Attach(   
   IDebugEventCallback2 pCallback  
);  
```  
  
#### Parameters  
 `pCallback`  
 [in] An [IDebugEventCallback2](../extensibility-debugger-reference/idebugeventcallback2.md) object to be used for debug event notification.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code. The following table shows some possible error codes.  
  
|Value|Description|  
|-----------|-----------------|  
|`E_ATTACH_DEBUGGER_ALREADY_ATTACHED`|The specified program is already attached to the debugger.|  
|`E_ATTACH_DEBUGGEE_PROCESS_SECURITY_VIOLATION`|A security violation occurred during the attach procedure.|  
|`E_ATTACH_CANNOT_ATTACH_TO_DESKTOP`|A desktop program cannot be attached to the debugger.|  
  
## Remarks  
 A debug engine (DE) never calls this method to attach to a program. If the DE runs in the program's address space, the [OnAttach](../extensibility-debugger-reference/idebugprogramnodeattach2--onattach.md) method is called. If the DE runs in the session debug manager's (SDM) address space, the [Attach](../extensibility-debugger-reference/idebugengine2--attach.md) method is called.  
  
## See Also  
 [IDebugProgram2](../extensibility-debugger-reference/idebugprogram2.md)   
 [IDebugEventCallback2](../extensibility-debugger-reference/idebugeventcallback2.md)   
 [OnAttach](../extensibility-debugger-reference/idebugprogramnodeattach2--onattach.md)   
 [Attach](../extensibility-debugger-reference/idebugengine2--attach.md)