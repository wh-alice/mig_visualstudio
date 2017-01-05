---
title: "IEnumDebugCodeContexts2"
ms.custom: ""
ms.date: "12/07/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "IEnumDebugCodeContexts2"
helpviewer_keywords: 
  - "IEnumDebugCodeContexts2"
ms.assetid: 72915146-215f-4c99-a034-131b2b474e0e
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
# IEnumDebugCodeContexts2
[!INCLUDE[vs2017banner](../../../code-quality/includes/vs2017banner.md)]

This interface enumerates the code contexts associated with the debug session, or with a particular program or document.  
  
## Syntax  
  
```  
IEnumDebugCodeContexts2 : IUnknown  
```  
  
## Notes for Implementers  
 The debug engine (DE) implements this interface to represent a list of code contexts for a particular text position in a program, or a list of code contexts for a particular document context.  
  
## Notes for Callers  
 Call [EnumCodeContexts](../../../extensibility/debugger/reference/idebugprogram2--enumcodecontexts.md) to obtain this interface representing a list of code contexts for a specific text position in a program's source document.  
  
 Call [EnumCodeContexts](../../../extensibility/debugger/reference/idebugdocumentcontext2--enumcodecontexts.md) to obtain this interface representing a list of all code contexts in a particular source document.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IEnumDebugCodeContexts2`.  
  
|Method|Description|  
|------------|-----------------|  
|[Next](../../../extensibility/debugger/reference/ienumdebugcodecontexts2--next.md)|Retrieves a specified number of code contexts in an enumeration sequence.|  
|[Skip](../../../extensibility/debugger/reference/ienumdebugcodecontexts2--skip.md)|Skips a specified number of code contexts in an enumeration sequence.|  
|[Reset](../../../extensibility/debugger/reference/ienumdebugcodecontexts2--reset.md)|Resets an enumeration sequence to the beginning.|  
|[Clone](../../../extensibility/debugger/reference/ienumdebugcodecontexts2--clone.md)|Creates an enumerator that contains the same enumeration state as the current enumerator.|  
|[GetCount](../../../extensibility/debugger/reference/ienumdebugcodecontexts2--getcount.md)|Gets the number of code contexts in an enumerator.|  
  
## Remarks  
 Visual Studio calls [EnumCodeContexts](../../../extensibility/debugger/reference/idebugprogram2--enumcodecontexts.md) to populate a list of code contexts the user can choose from when setting the next statement or showing the disassembly for a source file. Multiple code contexts can occur, for example, when there are multiple instances of a C++-style template.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../../../extensibility/debugger/reference/core-interfaces.md)   
 [EnumCodeContexts](../../../extensibility/debugger/reference/idebugprogram2--enumcodecontexts.md)   
 [EnumCodeContexts](../../../extensibility/debugger/reference/idebugdocumentcontext2--enumcodecontexts.md)