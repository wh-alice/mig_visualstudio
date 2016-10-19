---
title: "IDebugEngine2::Attach"
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
  - "IDebugEngine2::Attach"
helpviewer_keywords: 
  - "IDebugEngine2::Attach"
ms.assetid: 173dcbda-5019-4c5e-bca9-a071838b5739
caps.latest.revision: 14
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
# IDebugEngine2::Attach
Attaches a debug engine (DE) to a program or programs. Called by the session debug manager (SDM) when the DE is running in-process to the SDM.  
  
## Syntax  
  
```cpp#  
HRESULT Attach(   
   IDebugProgram2**      pProgram,  
   IDebugProgramNode2**  rgpProgramNodes,  
   DWORD                 celtPrograms,  
   IDebugEventCallback2* pCallback,  
   ATTACH_REASON         dwReason  
);  
```  
  
```c#  
int Attach(   
   IDebugProgram2[]     pProgram,  
   IDebugProgramNode2[] rgpProgramNodes,  
   uint                 celtPrograms,  
   IDebugEventCallback2 pCallback,  
   Enum_ATTACH_REASON   dwReason  
);  
```  
  
#### Parameters  
 `pProgram`  
 [in] An array of [IDebugProgram2](../extensibility/idebugprogram2.md) objects that represent programs to be attached to. These are port programs.  
  
 `rgpProgramNodes`  
 [in] An array of [IDebugProgramNode2](../extensibility/idebugprogramnode2.md) objects that represent program nodes, one for each program. The program nodes in this array represent the same programs as in `pProgram`. The program nodes are given so that the DE can identify the programs to attach to.  
  
 `celtPrograms`  
 [in] Number of programs and/or program nodes in the `pProgram` and `rgpProgramNodes` arrays.  
  
 `pCallback`  
 [in] The [IDebugEventCallback2](../extensibility/idebugeventcallback2.md) object to be used to send debug events to the SDM.  
  
 `dwReason`  
 [in] A value from the [ATTACH_REASON](../extensibility/attach_reason.md) enumeration that specifies the reason for attaching these programs. For more information, see the Remarks section.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 There are three reasons for attaching to a program, as follows:  
  
-   `ATTACH_REASON_LAUNCH` indicates that the DE is attaching to the program because the user launched the process that contains it.  
  
-   `ATTACH_REASON_USER` indicates that the user has explicitly requested the DE to attach to a program (or the process that contains a program).  
  
-   `ATTACH_REASON_AUTO` indicates the DE is attaching to a particular program because it is already debugging other programs in a particular process. This is also called auto-attach.  
  
 When this method is called, the DE needs to send these events in sequence:  
  
1.  [IDebugEngineCreateEvent2](../extensibility/idebugenginecreateevent2.md) (if it has not already been sent for a particular instance of the debug engine)  
  
2.  [IDebugProgramCreateEvent2](../extensibility/idebugprogramcreateevent2.md)  
  
3.  [IDebugLoadCompleteEvent2](../extensibility/idebugloadcompleteevent2.md)  
  
 In addition, if the reason for attaching is `ATTACH_REASON_LAUNCH`, the DE needs to send the [IDebugEntryPointEvent2](../extensibility/idebugentrypointevent2.md) event.  
  
 Once the DE gets the [IDebugProgramNode2](../extensibility/idebugprogramnode2.md) object corresponding to the program being debugged, it can be queried for any private interface.  
  
 Before calling the methods of a program node in the array given by `pProgram` or `rgpProgramNodes`, impersonation, if required, should be enabled on the `IDebugProgram2` interface that represents the program node. Normally, however, this step is not necessary. For more information, see [Security Issues](../extensibility/security-issues.md).  
  
## See Also  
 [IDebugEngine2](../extensibility/idebugengine2.md)   
 [IDebugProgramNode2](../extensibility/idebugprogramnode2.md)   
 [IDebugProgram2](../extensibility/idebugprogram2.md)   
 [IDebugEventCallback2](../extensibility/idebugeventcallback2.md)   
 [ATTACH_REASON](../extensibility/attach_reason.md)   
 [IDebugEngineCreateEvent2](../extensibility/idebugenginecreateevent2.md)   
 [IDebugProgramCreateEvent2](../extensibility/idebugprogramcreateevent2.md)   
 [IDebugLoadCompleteEvent2](../extensibility/idebugloadcompleteevent2.md)   
 [IDebugEntryPointEvent2](../extensibility/idebugentrypointevent2.md)