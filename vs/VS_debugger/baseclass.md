---
title: "BaseClass"
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
  - "user-defined types, base classes"
  - "BaseClass symbol"
  - "base classes, user-defined types"
ms.assetid: 9375ca35-cb91-45f5-8903-7344ee4528e8
caps.latest.revision: 16
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
# BaseClass
Each base class for a user-defined type (UDT) symbol is identified by a child with a `SymTagBaseClass` tag. The [IDiaSymbol::get_type](../VS_debugger/idiasymbol--get_type.md) property contains the symbol for the underlying UDT, and all properties of the underlying UDT are available as part of this BaseClass symbol.  
  
## Properties  
 The following table shows additional valid properties for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[IDiaSymbol::get_access](../VS_debugger/idiasymbol--get_access.md)|`DWORD`|Access modifier applied to this base class. One of the [CV_access_e Enumeration](../VS_debugger/cv_access_e.md) values.|  
|[IDiaSymbol::get_classParent](../VS_debugger/idiasymbol--get_classparent.md)|`IDiaSymbol*`|Symbol of the enclosing class (if any).|  
|[IDiaSymbol::get_classParentId](../VS_debugger/idiasymbol--get_classparentid.md)|`DWORD`|ID of the class parent symbol.|  
|[IDiaSymbol::get_constructor](../VS_debugger/idiasymbol--get_constructor.md)|`BOOL`|`TRUE` if the base class has a constructor.|  
|[IDiaSymbol::get_constType](../VS_debugger/idiasymbol--get_consttype.md)|`BOOL`|`TRUE` if the base class is marked as const.|  
|[IDiaSymbol::get_hasAssignmentOperator](../VS_debugger/idiasymbol--get_hasassignmentoperator.md)|`BOOL`|`TRUE` if the base class has an assignment operator.|  
|[IDiaSymbol::get_hasCastOperator](../VS_debugger/idiasymbol--get_hascastoperator.md)|`BOOL`|`TRUE` if the base class has a cast operator.|  
|[IDiaSymbol::get_hasNestedTypes](../VS_debugger/idiasymbol--get_hasnestedtypes.md)|`BOOL`|`TRUE` if the base class has nested types.|  
|[IDiaSymbol::get_indirectVirtualBaseClass](../VS_debugger/idiasymbol--get_indirectvirtualbaseclass.md)|`BOOL`|`TRUE` if the base class is indirect.|  
|[IDiaSymbol::get_length](../VS_debugger/idiasymbol--get_length.md)|`DWORD`|Length of this base class in bytes.|  
|[IDiaSymbol::get_lexicalParent](../VS_debugger/idiasymbol--get_lexicalparent.md)|`IDiaSymbol*`|Symbol of the enclosing compiland.|  
|[IDiaSymbol::get_lexicalParentId](../VS_debugger/idiasymbol--get_lexicalparentid.md)|`DWORD`|ID of the lexical parent symbol.|  
|[IDiaSymbol::get_name](../VS_debugger/idiasymbol--get_name.md)|`BSTR`|Name of the base class.|  
|[IDiaSymbol::get_nested](../VS_debugger/idiasymbol--get_nested.md)|`BOOL`|`TRUE` if the base class is nested.|  
|[IDiaSymbol::get_offset](../VS_debugger/idiasymbol--get_offset.md)|`LONG`|Offset of subobject that represents the base class within the structure.|  
|[IDiaSymbol::get_overloadedOperator](../VS_debugger/idiasymbol--get_overloadedoperator.md)|`BOOL`|`TRUE` if the base class has any overloaded operators.|  
|[IDiaSymbol::get_packed](../VS_debugger/idiasymbol--get_packed.md)|`BOOL`|`TRUE` if the base class is packed.|  
|[IDiaSymbol::get_scoped](../VS_debugger/idiasymbol--get_scoped.md)|`BOOL`|`TRUE` if the base class appears in a nonglobal scope.|  
|[IDiaSymbol::get_symIndexId](../VS_debugger/idiasymbol--get_symindexid.md)|`DWORD`|Index ID of symbol.|  
|[IDiaSymbol::get_symTag](../VS_debugger/idiasymbol--get_symtag.md)|`DWORD`|Returns `SymTagBaseClass` (one of the [SymTagEnum Enumeration](../VS_debugger/symtagenum.md) values).|  
|[IDiaSymbol::get_type](../VS_debugger/idiasymbol--get_type.md)|`IDiaSymbol*`|The symbol for the base class [UDT](../VS_debugger/udt.md).|  
|[IDiaSymbol::get_typeId](../VS_debugger/idiasymbol--get_typeid.md)|`DWORD`|ID of the type symbol.|  
|[IDiaSymbol::get_udtKind](../VS_debugger/idiasymbol--get_udtkind.md)|`DWORD`|A value from the [UdtKind Enumeration](../VS_debugger/udtkind.md).|  
|[IDiaSymbol::get_unalignedType](../VS_debugger/idiasymbol--get_unalignedtype.md)|`BOOL`|`TRUE` if the base class is unaligned.|  
|[IDiaSymbol::get_virtualBaseClass](../VS_debugger/idiasymbol--get_virtualbaseclass.md)|`BOOL`|`TRUE` if the base class is virtual.|  
|[IDiaSymbol::get_virtualBaseDispIndex](../VS_debugger/idiasymbol--get_virtualbasedispindex.md)|`DWORD`|Index into the virtual base displacement table.|  
|[IDiaSymbol::get_virtualBasePointerOffset](../VS_debugger/idiasymbol--get_virtualbasepointeroffset.md)|`LONG`|Offset of the virtual base pointer.|  
|[IDiaSymbol::get_virtualBaseTableType](../VS_debugger/idiasymbol--get_virtualbasetabletype.md)|`IDiaSymbol*`|The type of the virtual base table pointer.|  
|[IDiaSymbol::get_virtualTableShape](../VS_debugger/idiasymbol--get_virtualtableshape.md)|`IDiaSymbol*`|The symbol describing the type of the virtual table for this base class.|  
|[IDiaSymbol::get_virtualTableShapeId](../VS_debugger/idiasymbol--get_virtualtableshapeid.md)|`DWORD`|ID of the virtual table shape symbol.|  
|[IDiaSymbol::get_volatileType](../VS_debugger/idiasymbol--get_volatiletype.md)|`BOOL`|`TRUE` if the base class is marked as volatile.|  
  
## See Also  
 [Class Hierarchy of Symbol Types](../VS_debugger/class-hierarchy-of-symbol-types.md)   
 [UDT](../VS_debugger/udt.md)