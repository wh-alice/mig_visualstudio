---
title: "Class Hierarchy of Symbol Types | hehe"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
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
|[UDT](../debug-interface-access/udt.md)|Symbol used to represent each class, structure, and union.|  
|[Enum (Debug Interface Access SDK)](../debug-interface-access/enum--debug-interface-access-sdk-.md)|Symbol for enumerated types.|  
|[PointerType](../debug-interface-access/pointertype.md)|Symbol for pointer types.|  
|[ArrayType](../debug-interface-access/arraytype.md)|Symbol for array types.|  
|[BaseType](../debug-interface-access/basetype.md)|Symbol for base types|  
|[Typedef (Debug Interface Access SDK)](../debug-interface-access/typedef--debug-interface-access-sdk-.md)|Symbol that introduces names for other types.|  
|[BaseClass](../debug-interface-access/baseclass.md)|Symbol used for each base class of a user-defined type (UDT).|  
|[Friend (Debug Interface Access SDK)](../debug-interface-access/friend--debug-interface-access-sdk-.md)|Symbol for friend classes and friend functions.|  
|[FunctionType](../debug-interface-access/functiontype.md)|Symbol for each unique function signature.|  
|[FunctionArgType](../debug-interface-access/functionargtype.md)|Symbol for each parameter to a function.|  
|[VTableShape](../debug-interface-access/vtableshape.md)|Symbol for the size of the virtual table.|  
|[VTable](../debug-interface-access/vtable.md)|Symbol for a virtual table.|  
|[CustomType](../debug-interface-access/customtype.md)|Symbol for vendor-defined type.|  
|[ManagedType](../debug-interface-access/managedtype.md)|Symbol for a type defined in metadata.|  
|[Dimension](../debug-interface-access/dimension.md)|Symbol for array dimensions.|  
  
> [!NOTE]
>  Each symbol can have properties that hold information about the symbol, as well as references to other symbols. These properties are listed in the individual symbol topics.  
  
## See Also  
 [CV_access_e Enumeration](../debug-interface-access/cv_access_e.md)   
 [Lexical Hierarchy of Symbol Types](../debug-interface-access/lexical-hierarchy-of-symbol-types.md)   
 [Symbols and Symbol Tags](../debug-interface-access/symbols-and-symbol-tags.md)