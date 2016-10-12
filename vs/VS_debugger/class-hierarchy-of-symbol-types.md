---
title: "Class Hierarchy of Symbol Types"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: na
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "symbols [DIA SDK], class hierarchies"
ms.assetid: 0ccd6990-4654-44cd-a6f3-bdd82fe90f6c
caps.latest.revision: 10
ms.author: "mikejo"
manager: "ghogen"
translation.priority.ht: 
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "ru-ru"
  - "zh-cn"
  - "zh-tw"
translation.priority.mt: 
  - "cs-cz"
  - "pl-pl"
  - "pt-br"
  - "tr-tr"
---
# Class Hierarchy of Symbol Types
The following table describes the symbol types in the class hierarchy.  
  
## Symbol Types  
  
|Symbol type|Description|  
|-----------------|-----------------|  
|[UDT](../VS_debugger/udt.md)|Symbol used to represent each class, structure, and union.|  
|[Enum (Debug Interface Access SDK)](../VS_debugger/enum--debug-interface-access-sdk-.md)|Symbol for enumerated types.|  
|[PointerType](../VS_debugger/pointertype.md)|Symbol for pointer types.|  
|[ArrayType](../VS_debugger/arraytype.md)|Symbol for array types.|  
|[BaseType](../VS_debugger/basetype.md)|Symbol for base types|  
|[Typedef (Debug Interface Access SDK)](../VS_debugger/typedef--debug-interface-access-sdk-.md)|Symbol that introduces names for other types.|  
|[BaseClass](../VS_debugger/baseclass.md)|Symbol used for each base class of a user-defined type (UDT).|  
|[Friend (Debug Interface Access SDK)](../VS_debugger/friend--debug-interface-access-sdk-.md)|Symbol for friend classes and friend functions.|  
|[FunctionType](../VS_debugger/functiontype.md)|Symbol for each unique function signature.|  
|[FunctionArgType](../VS_debugger/functionargtype.md)|Symbol for each parameter to a function.|  
|[VTableShape](../VS_debugger/vtableshape.md)|Symbol for the size of the virtual table.|  
|[VTable](../VS_debugger/vtable.md)|Symbol for a virtual table.|  
|[CustomType](../VS_debugger/customtype.md)|Symbol for vendor-defined type.|  
|[ManagedType](../VS_debugger/managedtype.md)|Symbol for a type defined in metadata.|  
|[Dimension](../VS_debugger/dimension.md)|Symbol for array dimensions.|  
  
> [!NOTE]
>  Each symbol can have properties that hold information about the symbol, as well as references to other symbols. These properties are listed in the individual symbol topics.  
  
## See Also  
 [CV_access_e Enumeration](../VS_debugger/cv_access_e.md)   
 [Lexical Hierarchy of Symbol Types](../VS_debugger/lexical-hierarchy-of-symbol-types.md)   
 [Symbols and Symbol Tags](../VS_debugger/symbols-and-symbol-tags.md)