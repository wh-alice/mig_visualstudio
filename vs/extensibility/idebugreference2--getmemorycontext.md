---
title: "IDebugReference2::GetMemoryContext | Microsoft Docs"
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
  - "IDebugReference2::GetMemoryContext"
helpviewer_keywords: 
  - "IDebugReference2::GetMemoryContext"
ms.assetid: 47fc3827-07a0-4eee-b7f4-fc1c62e6b25c
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
# IDebugReference2::GetMemoryContext
Gets a memory context of a reference. Reserved for future use.  
  
## Syntax  
  
```cpp#  
HRESULT GetMemoryContext (   
   IDebugMemoryContext2** ppMemory  
);  
```  
  
```c#  
int GetMemoryContext (   
   out IDebugMemoryContext2 ppMemory  
);  
```  
  
#### Parameters  
 `ppMemory`  
 [out] Returns the [IDebugMemoryContext2](../extensibility/idebugmemorycontext2.md) object that represents the memory associated with the value of the reference.  
  
## Return Value  
 Always returns `E_NOTIMPL`.  
  
## See Also  
 [IDebugReference2](../extensibility/idebugreference2.md)   
 [IDebugMemoryContext2](../extensibility/idebugmemorycontext2.md)