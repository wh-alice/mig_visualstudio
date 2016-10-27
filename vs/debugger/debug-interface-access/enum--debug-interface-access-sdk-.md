---
title: "Enum (Debug Interface Access SDK)"
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
  - "enumerated types as symbols"
  - "Enum symbol"
ms.assetid: c777e2e6-88be-435b-b632-8d43f42b0b49
caps.latest.revision: 15
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
# Enum (Debug Interface Access SDK)
Enumerations are identified by `SymTagEnum` symbols. Each enumeration value appears as a class child with a `SymTagConstant` tag.  
  
## Properties  
 The following table shows additional valid properties for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[IDiaSymbol::get_baseType](../../debugger/debug-interface-access/idiasymbol--get_basetype.md)|`DWORD`|One of the [BasicType Enumeration](../../debugger/debug-interface-access/basictype.md) values.|  
|[IDiaSymbol::get_classParent](../../debugger/debug-interface-access/idiasymbol--get_classparent.md)|`IDiaSymbol*`|Class parent of this enumeration, if any.|  
|[IDiaSymbol::get_classParentId](../../debugger/debug-interface-access/idiasymbol--get_classparentid.md)|`DWORD`|ID of the class parent symbol.|  
|[IDiaSymbol::get_constructor](../../debugger/debug-interface-access/idiasymbol--get_constructor.md)|`BOOL`|`TRUE` if the enumeration has a constructor.|  
|[IDiaSymbol::get_constType](../../debugger/debug-interface-access/idiasymbol--get_consttype.md)|`BOOL`|`TRUE` if the enumeration is marked as const.|  
|[IDiaSymbol::get_hasAssignmentOperator](../../debugger/debug-interface-access/idiasymbol--get_hasassignmentoperator.md)|`BOOL`|`TRUE` if the enumeration has an assignment operator.|  
|[IDiaSymbol::get_hasCastOperator](../../debugger/debug-interface-access/idiasymbol--get_hascastoperator.md)|`BOOL`|`TRUE` if the enumeration has a cast operator.|  
|[IDiaSymbol::get_hasNestedTypes](../../debugger/debug-interface-access/idiasymbol--get_hasnestedtypes.md)|`BOOL`|`TRUE` if the enumeration has nested types.|  
|[IDiaSymbol::get_length](../../debugger/debug-interface-access/idiasymbol--get_length.md)|`DWORD`|Length of this enumeration in bytes.|  
|[IDiaSymbol::get_lexicalParent](../../debugger/debug-interface-access/idiasymbol--get_lexicalparent.md)|`IDiaSymbol*`|Symbol of the enclosing [Compiland](../../debugger/debug-interface-access/compiland.md).|  
|[IDiaSymbol::get_lexicalParentId](../../debugger/debug-interface-access/idiasymbol--get_lexicalparentid.md)|`DWORD`|ID of the lexical parent symbol.|  
|[IDiaSymbol::get_name](../../debugger/debug-interface-access/idiasymbol--get_name.md)|`BSTR`|Name of the enumerated type.|  
|[IDiaSymbol::get_nested](../../debugger/debug-interface-access/idiasymbol--get_nested.md)|`BOOL`|`TRUE` if the enumeration is nested.|  
|[IDiaSymbol::get_overloadedOperator](../../debugger/debug-interface-access/idiasymbol--get_overloadedoperator.md)|`BOOL`|`TRUE` if the enumeration has any overloaded operators.|  
|[IDiaSymbol::get_packed](../../debugger/debug-interface-access/idiasymbol--get_packed.md)|`BOOL`|`TRUE` if the enumeration is packed.|  
|[IDiaSymbol::get_scoped](../../debugger/debug-interface-access/idiasymbol--get_scoped.md)|`BOOL`|`TRUE` if the enumeration appears in a nonglobal lexical scope.|  
|[IDiaSymbol::get_symIndexId](../../debugger/debug-interface-access/idiasymbol--get_symindexid.md)|`DWORD`|Index ID of symbol.|  
|[IDiaSymbol::get_symTag](../../debugger/debug-interface-access/idiasymbol--get_symtag.md)|`DWORD`|Returns `SymTagEnum` (one of the [SymTagEnum Enumeration](../../debugger/debug-interface-access/symtagenum.md) values).|  
|[IDiaSymbol::get_type](../../debugger/debug-interface-access/idiasymbol--get_type.md)|`IDiaSymbol*`|Symbol for the underlying type.|  
|[IDiaSymbol::get_typeId](../../debugger/debug-interface-access/idiasymbol--get_typeid.md)|`DWORD`|ID of the type symbol.|  
|[IDiaSymbol::get_unalignedType](../../debugger/debug-interface-access/idiasymbol--get_unalignedtype.md)|`BOOL`|`TRUE` if the enumeration is unaligned.|  
|[IDiaSymbol::get_volatileType](../../debugger/debug-interface-access/idiasymbol--get_volatiletype.md)|`BOOL`|`TRUE` if the enumeration is marked as volatile.|  
  
## See Also  
 [Class Hierarchy of Symbol Types](../../debugger/debug-interface-access/class-hierarchy-of-symbol-types.md)