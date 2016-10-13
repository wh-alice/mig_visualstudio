---
title: "BSTR_ARRAY"
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
  - "BSTR_ARRAY"
helpviewer_keywords: 
  - "BSTR_ARRAY structure"
ms.assetid: 48da37f7-a237-48a9-9ff9-389c1a00862c
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
# BSTR_ARRAY
A structure that describes an array of strings.  
  
## Syntax  
  
```cpp#  
typedef struct tagBSTR_ARRAY {  
   DWORD dwCount;  
   BSTR* Members;  
} BSTR_ARRAY;  
```  
  
```c#  
struct BSTR_ARRAY {  
   DWORD    dwCount;  
   string[] Members;  
}  
```  
  
## Terms  
 dwCount  
 Number of strings in `Members` array.  
  
 Members  
 Array of strings.  
  
## Remarks  
 This structure is returned from the [EnumPersistedPorts](../extensibility/idebugportsupplier3--enumpersistedports.md) method.  
  
 [C++ only] Each individual string must be freed using `SysFreeString`, and the `Members` array must be freed with `CoTaskMemFree`.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../extensibility/structures-and-unions.md)   
 [EnumPersistedPorts](../extensibility/idebugportsupplier3--enumpersistedports.md)