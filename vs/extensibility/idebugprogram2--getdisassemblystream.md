---
title: "IDebugProgram2::GetDisassemblyStream | Microsoft Docs"
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
  - "IDebugProgram2::GetDisassemblyStream"
helpviewer_keywords: 
  - "IDebugProgram2::GetDisassemblyStream"
ms.assetid: beda0da5-267e-4bf3-96c4-b659d29e2254
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
# IDebugProgram2::GetDisassemblyStream
Gets the disassembly stream for this program or a part of this program.  
  
## Syntax  
  
```cpp#  
HRESULT GetDisassemblyStream(   
   DISASSEMBLY_STREAM_SCOPE   dwScope,  
   IDebugCodeContext2*        pCodeContext,  
   IDebugDisassemblyStream2** ppDisassemblyStream  
);  
```  
  
```c#  
int GetDisassemblyStream(   
   enum_DISASSEMBLY_STREAM_SCOPE  dwScope,  
   IDebugCodeContext2             pCodeContext,  
   out IDebugDisassemblyStream2   ppDisassemblyStream  
);  
```  
  
#### Parameters  
 `dwScope`  
 [in] Specifies a value from the [DISASSEMBLY_STREAM_SCOPE](../extensibility/disassembly_stream_scope.md) enumeration that defines the scope of the disassembly stream.  
  
 `pCodeContext`  
 [in] An [IDebugCodeContext2](../extensibility/idebugcodecontext2.md) object that represents the position of where to start the disassembly stream.  
  
 `ppDisassemblyStream`  
 [out] Returns an [IDebugDisassemblyStream2](../extensibility/idebugdisassemblystream2.md) object that represents the disassembly stream.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code. Returns `E_DISASM_NOTSUPPORTED` if disassembly is not supported for this particular architecture.  
  
## Remarks  
 If the `dwScopes` parameter has the `DSS_HUGE` flag of the [DISASSEMBLY_STREAM_SCOPE](../extensibility/disassembly_stream_scope.md) enumeration set, then the disassembly is expected to return a large number of disassembly instructions, for example, for an entire file or module. If the `DSS_HUGE` flag is not set, then the disassembly is expected to be confined to a small region, typically that of a single function.  
  
## See Also  
 [IDebugProgram2](../extensibility/idebugprogram2.md)   
 [DISASSEMBLY_STREAM_SCOPE](../extensibility/disassembly_stream_scope.md)   
 [IDebugCodeContext2](../extensibility/idebugcodecontext2.md)   
 [IDebugDisassemblyStream2](../extensibility/idebugdisassemblystream2.md)