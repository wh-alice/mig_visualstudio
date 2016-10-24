---
title: "IDebugDisassemblyStream2::Read | testtitle"
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
  - "IDebugDisassemblyStream2::Read"
helpviewer_keywords: 
  - "IDebugDisassemblyStream2::Read"
ms.assetid: 7db5f6bb-73ee-45bc-b187-c1b6aa2dfdd5
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
# IDebugDisassemblyStream2::Read
Reads instructions starting from the current position in the disassembly stream.  
  
## Syntax  
  
```cpp#  
HRESULT Read(   
   DWORD                     dwInstructions,  
   DISASSEMBLY_STREAM_FIELDS dwFields,  
   DWORD*                    pdwInstructionsRead,  
   DisassemblyData*          prgDisassembly  
);  
```  
  
```c#  
int Read(   
   uint                           dwInstructions,  
   enum_DISASSEMBLY_STREAM_FIELDS dwFields,  
   out uint                       pdwInstructionsRead,  
   DisassemblyData[]              prgDisassembly  
);  
```  
  
#### Parameters  
 `dwInstructions`  
 [in] The number of instructions to disassemble. This value is also the maximum length of the `prgDisassembly` array.  
  
 `dwFields`  
 [in] A combination of flags from the [DISASSEMBLY_STREAM_FIELDS](../extensibility-debugger-reference/disassembly_stream_fields.md) enumeration that indicate which fields of `prgDisassembly` are to be filled out.  
  
 `pdwInstructionsRead`  
 [out] Returns the number of instructions actually disassembled.  
  
 `prgDisassembly`  
 [out] An array of [DisassemblyData](../extensibility-debugger-reference/disassemblydata.md) structures that is filled in with the disassembled code, one structure per disassembled instruction. The length of this array is dictated by the `dwInstructions` parameter.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 The maximum number of instructions that are available in the current scope can be obtained by calling the [GetSize](../extensibility-debugger-reference/idebugdisassemblystream2--getsize.md) method.  
  
 The current position where the next instruction is read from can be changed by calling the [Seek](../extensibility-debugger-reference/idebugdisassemblystream2--seek.md) method.  
  
 The `DSF_OPERANDS_SYMBOLS` flag can be added to the `DSF_OPERANDS` flag in the `dwFields` parameter to indicate that symbol names should be used when disassembling instructions.  
  
## See Also  
 [IDebugDisassemblyStream2](../extensibility-debugger-reference/idebugdisassemblystream2.md)   
 [DISASSEMBLY_STREAM_FIELDS](../extensibility-debugger-reference/disassembly_stream_fields.md)   
 [DisassemblyData](../extensibility-debugger-reference/disassemblydata.md)   
 [GetSize](../extensibility-debugger-reference/idebugdisassemblystream2--getsize.md)   
 [Seek](../extensibility-debugger-reference/idebugdisassemblystream2--seek.md)