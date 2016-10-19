---
title: "IDebugProgramEx2::Attach"
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
  - "IDebugProgramEx2::Attach"
helpviewer_keywords: 
  - "IDebugProgramEx2::Attach"
ms.assetid: 33b22b2f-431e-4205-9441-d28a9c928c97
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
# IDebugProgramEx2::Attach
Attach a session to a program.  
  
## Syntax  
  
```cpp#  
HRESULT Attach(   
   IDebugEventCallback2* pCallback,  
   DWORD                 dwReason,  
   IDebugSession2*       pSession  
);  
```  
  
```  
[C#]  
int Attach(   
   IDebugEventCallback2 pCallback,  
   uint                 dwReason,  
   IDebugSession2       pSession  
);  
```  
  
#### Parameters  
 `pCallback`  
 [in] An [IDebugEventCallback2](../extensibility/idebugeventcallback2.md) object that represents the callback function that the attached debug engine sends events to.  
  
 `dwReason`  
 [in] A value from the [ATTACH_REASON](../extensibility/attach_reason.md) enumeration that describes the reason for the attach operation.  
  
 `pSession`  
 [in] A value that uniquely identifies the session that is attaching to the program.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise returns an error code. This method should return `E_ATTACH_DEBUGGER_ALREADY_ATTACHED` if the program is already attached.  
  
## Remarks  
 The port that contains the program can use the value in `pSession` to determine which session is attempting to attach to the program. For example, if a port allows only one debug session to attach to a process at a time, the port can determine if the same session is already attached to other programs in the process.  
  
> [!NOTE]
>  The interface passed in `pSession` is to be treated only as a cookie, a value that uniquely identifies the session debug manager attaching to this program; none of the methods on the supplied interface are functional.  
  
## See Also  
 [IDebugProgramEx2](../extensibility/idebugprogramex2.md)