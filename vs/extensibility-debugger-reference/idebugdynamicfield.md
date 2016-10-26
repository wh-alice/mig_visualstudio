---
title: "IDebugDynamicField"
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
  - "IDebugDynamicField"
helpviewer_keywords: 
  - "IDebugDynamicField interface"
ms.assetid: caffbd95-7596-4714-84b1-b964e89a78bb
caps.latest.revision: 7
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
# IDebugDynamicField
This interface represents a type of a variable.  
  
## Syntax  
  
```  
IDebugDynamicField : IDebugField  
```  
  
## Notes for Implementers  
 This interface is implemented by symbol providers as a base class for any type that can be determined at run time. This is for managed code only.  
  
## Notes for Callers  
 This interface represents a base class from which more specialized interfaces can be derived.  
  
## Methods in Vtable order  
 This interface does not supply any methods other than those inherited from `IDebugField`.  
  
## Requirements  
 Header: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Symbol Provider Interfaces](../extensibility-debugger-reference/symbol-provider-interfaces.md)   
 [IDebugField](../extensibility-debugger-reference/idebugfield.md)