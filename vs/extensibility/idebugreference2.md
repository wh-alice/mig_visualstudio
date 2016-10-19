---
title: "IDebugReference2"
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
  - "IDebugReference2"
helpviewer_keywords: 
  - "IDebugReference2 interface"
ms.assetid: 3cfed312-f532-4bce-84a5-1677c14567d7
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
# IDebugReference2
This interface represents a reference to a stack frame property or some other property.  
  
> [!NOTE]
>  `IDebugReference2` is reserved for future use, and all its methods should return `E_NOTIMPL`.  
  
## Syntax  
  
```  
IDebugReference2 : IUnknown  
```  
  
## Notes for Implementers  
 The DE implements this interface to represent a reference to a particular kind of value. For example, the value could be a numerical value as a result of an expression evaluation, a memory context used for displaying memory, or a list of registers and their values.  
  
## Notes for Callers  
 Call [GetReference](../extensibility/idebugproperty2--getreference.md) to obtain this interface. [GetParent](../extensibility/idebugreference2--getparent.md) and [GetDerivedMostReference](../extensibility/idebugreference2--getderivedmostreference.md) also return this interface.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugReference2`.  
  
|Method|Description|  
|------------|-----------------|  
|[GetReferenceInfo](../extensibility/idebugreference2--getreferenceinfo.md)|Gets the [DEBUG_REFERENCE_INFO](../extensibility/debug_reference_info.md) structure that describes this reference.|  
|[SetValueAsString](../extensibility/idebugreference2--setvalueasstring.md)|Sets the value of this reference from a string.|  
|[SetValueAsReference](../extensibility/idebugreference2--setvalueasreference.md)|Sets the value of this reference from another reference.|  
|[EnumChildren](../extensibility/idebugreference2--enumchildren.md)|Enumerates the children of this reference.|  
|[GetParent](../extensibility/idebugreference2--getparent.md)|Gets the parent of this reference.|  
|[GetDerivedMostReference](../extensibility/idebugreference2--getderivedmostreference.md)|Gets the most-derived reference of this reference.|  
|[GetMemoryBytes](../extensibility/idebugreference2--getmemorybytes.md)|Gets the memory bytes to which this reference refers.|  
|[GetMemoryContext](../extensibility/idebugreference2--getmemorycontext.md)|Gets a memory context for this reference.|  
|[GetSize](../extensibility/idebugreference2--getsize.md)|Gets the size, in bytes, of this reference.|  
|[SetReferenceType](../extensibility/idebugreference2--setreferencetype.md)|Sets this reference type.|  
|[Compare](../extensibility/idebugreference2--compare.md)|Compares this reference with another.|  
  
## Remarks  
  
> [!NOTE]
>  This use of "property" should not be confused with that meaning a member variable of a class, although an `IDebugReference2` can represent such an entity.  
  
 [IDebugProperty2](../extensibility/idebugproperty2.md) represents a property, while `IDebugReference2` represents a reference to a property, typically a reference to an object in the program being debugged.  
  
 The main difference between a property and a reference is that a property refers to a named instance of an object, while a reference refers to an unnamed instance. For example, a property may refer to an object in the program's heap by `"a.b"`. Another property may refer to the same object as `"c.d"`. The way of referring to this property requires that `"a.b"` or `"c.d"` be in scope. A reference to this same object is nameless; the object can be referred to as long as the memory for that object is valid.  
  
 An `IDebugProperty2` interface can be thought of as a value with a name, a type, and an address. An `IDebugReference2`, on the other hand, can be thought of as a type and an address.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../extensibility/core-interfaces.md)   
 [DEBUG_REFERENCE_INFO](../extensibility/debug_reference_info.md)   
 [IDebugProperty2](../extensibility/idebugproperty2.md)   
 [GetReference](../extensibility/idebugproperty2--getreference.md)