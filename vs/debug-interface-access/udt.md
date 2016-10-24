---
title: "UDT"
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
  - "SymTagUDT symbol"
  - "user-defined type (UDT) symbol"
  - "unions, as symbols"
  - "UDT symbol"
  - "structs [C++]"
ms.assetid: f12459dd-c64d-4cc9-9ee3-a56e19e9e573
caps.latest.revision: 17
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
# UDT
Each class, structure, and union is identified by a `SymTagUDT` symbol. Each member, function, data, or nested type, and each base class, appears as a class child of the user-defined type (UDT).  
  
## Properties  
 The following table shows additional valid properties for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[IDiaSymbol::get_classParent](../debug-interface-access/idiasymbol--get_classparent.md)|`IDiaSymbol*`|Symbol for the class parent, if any.|  
|[IDiaSymbol::get_classParentId](../debug-interface-access/idiasymbol--get_classparentid.md)|`DWORD`|ID of the class parent symbol.|  
|[IDiaSymbol::get_constructor](../debug-interface-access/idiasymbol--get_constructor.md)|`BOOL`|`TRUE` if the UDT has a constructor.|  
|[IDiaSymbol::get_constType](../debug-interface-access/idiasymbol--get_consttype.md)|`BOOL`|`TRUE` if the UDT is marked as constant.|  
|[IDiaSymbol::get_hasAssignmentOperator](../debug-interface-access/idiasymbol--get_hasassignmentoperator.md)|`BOOL`|`TRUE` if the UDT has any assignment operators defined.|  
|[IDiaSymbol::get_hasCastOperator](../debug-interface-access/idiasymbol--get_hascastoperator.md)|`BOOL`|`TRUE` if the UDT has any cast operators defined.|  
|[IDiaSymbol::get_hasNestedTypes](../debug-interface-access/idiasymbol--get_hasnestedtypes.md)|`BOOL`|`TRUE` if the UDT has nested type definitions.|  
|[IDiaSymbol::get_length](../debug-interface-access/idiasymbol--get_length.md)|`LONGLONG`|The size, in bytes, of the UDT.|  
|[IDiaSymbol::get_lexicalParent](../debug-interface-access/idiasymbol--get_lexicalparent.md)|`IDiaSymbol*`|Symbol of the enclosing [Compiland](../debug-interface-access/compiland.md).|  
|[IDiaSymbol::get_lexicalParentId](../debug-interface-access/idiasymbol--get_lexicalparentid.md)|`DWORD`|ID of the lexical parent symbol.|  
|[IDiaSymbol::get_name](../debug-interface-access/idiasymbol--get_name.md)|`BSTR`|The name of the UDT.|  
|[IDiaSymbol::get_nested](../debug-interface-access/idiasymbol--get_nested.md)|`BOOL`|`TRUE` if the UDT is nested.|  
|[IDiaSymbol::get_overloadedOperator](../debug-interface-access/idiasymbol--get_overloadedoperator.md)|`BOOL`|`TRUE` if overloaded operators are defined for the UDT.|  
|[IDiaSymbol::get_packed](../debug-interface-access/idiasymbol--get_packed.md)|`BOOL`|`TRUE` if the UDT is packed.|  
|[IDiaSymbol::get_scoped](../debug-interface-access/idiasymbol--get_scoped.md)|`BOOL`|`TRUE` if the UDT appears in a nonglobal lexical scope.|  
|[IDiaSymbol::get_symIndexId](../debug-interface-access/idiasymbol--get_symindexid.md)|`DWORD`|Index ID of symbol.|  
|[IDiaSymbol::get_symTag](../debug-interface-access/idiasymbol--get_symtag.md)|`DWORD`|Returns `SymTagUDT` (one of the [SymTagEnum Enumeration](../debug-interface-access/symtagenum.md) values).|  
|[IDiaSymbol::get_udtKind](../debug-interface-access/idiasymbol--get_udtkind.md)|`DWORD`|Indicates whether this is a structure, class, or union; for details, see [UdtKind Enumeration](../debug-interface-access/udtkind.md).|  
|[IDiaSymbol::get_unalignedType](../debug-interface-access/idiasymbol--get_unalignedtype.md)|`BOOL`|`TRUE` if the UDT is unaligned.|  
|[IDiaSymbol::get_virtualTableShape](../debug-interface-access/idiasymbol--get_virtualtableshape.md)|`IDiaSymbol*`|The type of the virtual table.|  
|[IDiaSymbol::get_virtualTableShapeId](../debug-interface-access/idiasymbol--get_virtualtableshapeid.md)|`DWORD`|ID of the virtual table shape symbol.|  
|[IDiaSymbol::get_volatileType](../debug-interface-access/idiasymbol--get_volatiletype.md)|`BOOL`|`TRUE` if the UDT is marked as volatile.|  
  
## See Also  
 [Class Hierarchy of Symbol Types](../debug-interface-access/class-hierarchy-of-symbol-types.md)