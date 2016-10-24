---
title: "IEnumCodePaths2 | testtitle"
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
  - "IEnumCodePaths2"
helpviewer_keywords: 
  - "IEnumCodePaths2 interface"
ms.assetid: 17ec9f9e-dc06-4532-b5db-da52efcc8630
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
# IEnumCodePaths2
This interface represents a list of code paths.  
  
## Syntax  
  
```  
IEnumCodePaths2 : IUnknown  
```  
  
## Notes for Implementers  
 The debug engine (DE) implements this interface to represent a list of code paths.  
  
## Notes for Callers  
 Call [EnumCodePaths](../extensibility-debugger-reference/idebugprogram2--enumcodepaths.md) to obtain this interface.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IEnumCodePaths2`.  
  
|Method|Description|  
|------------|-----------------|  
|[Next](../extensibility-debugger-reference/ienumcodepaths2--next.md)|Retrieves a specified number of code paths in an enumeration sequence.|  
|[Skip](../extensibility-debugger-reference/ienumcodepaths2--skip.md)|Skips a specified number of code paths in an enumeration sequence.|  
|[Reset](../extensibility-debugger-reference/ienumcodepaths2--reset.md)|Resets an enumeration sequence to the beginning.|  
|[Clone](../extensibility-debugger-reference/ienumcodepaths2--clone.md)|Creates an enumerator that contains the same enumeration state as the current enumerator.|  
|[GetCount](../extensibility-debugger-reference/ienumcodepaths2--getcount.md)|Gets the number of code paths in an enumerator.|  
  
## Remarks  
 A code path represents a branch point or function call in a program. A list of code paths represents the path through which the code execution has taken.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../extensibility-debugger-reference/core-interfaces.md)