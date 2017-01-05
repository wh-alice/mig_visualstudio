---
title: "Typedef (Debug Interface Access SDK)"
ms.custom: ""
ms.date: "12/07/2016"
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
  - "Typedef symbol [DIA SDK]"
ms.assetid: 9ab441b9-cc72-47fa-83e2-87b3c2b891b4
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
# Typedef (Debug Interface Access SDK)
[!INCLUDE[vs2017banner](../../code-quality/includes/vs2017banner.md)]

Symbols with `SymTagTypedef` tags introduce names for other types.  
  
## Properties  
 The following table shows additional valid properties for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[IDiaSymbol::get_baseType](../../debugger/debug-interface-access/idiasymbol--get_basetype.md)|`DWORD`|One of the [BasicType Enumeration](../../debugger/debug-interface-access/basictype.md) values.|  
|[IDiaSymbol::get_classParent](../../debugger/debug-interface-access/idiasymbol--get_classparent.md)|`IDiaSymbol*`|Class parent of this typedef, if any.|  
|[IDiaSymbol::get_classParentId](../../debugger/debug-interface-access/idiasymbol--get_classparentid.md)|`DWORD`|ID of the class parent symbol.|  
|[IDiaSymbol::get_constructor](../../debugger/debug-interface-access/idiasymbol--get_constructor.md)|`BOOL`|`TRUE` if this typedef has a constructor.|  
|[IDiaSymbol::get_constType](../../debugger/debug-interface-access/idiasymbol--get_consttype.md)|`BOOL`|`TRUE` if this typedef is marked as constant.|  
|[IDiaSymbol::get_hasAssignmentOperator](../../debugger/debug-interface-access/idiasymbol--get_hasassignmentoperator.md)|`BOOL`|`TRUE` if this typedef has an assignment operator.|  
|[IDiaSymbol::get_hasCastOperator](../../debugger/debug-interface-access/idiasymbol--get_hascastoperator.md)|`BOOL`|`TRUE` if this typedef has a cast operator.|  
|[IDiaSymbol::get_hasNestedTypes](../../debugger/debug-interface-access/idiasymbol--get_hasnestedtypes.md)|`BOOL`|`TRUE` if this typedef has nested types.|  
|[IDiaSymbol::get_length](../../debugger/debug-interface-access/idiasymbol--get_length.md)|`ULONGLONG`|Length of this typedef in bytes.|  
|[IDiaSymbol::get_lexicalParent](../../debugger/debug-interface-access/idiasymbol--get_lexicalparent.md)|`IDiaSymbol*`|Symbol of the enclosing compiland.|  
|[IDiaSymbol::get_lexicalParentId](../../debugger/debug-interface-access/idiasymbol--get_lexicalparentid.md)|`DWORD`|ID of the lexical parent symbol.|  
|[IDiaSymbol::get_name](../../debugger/debug-interface-access/idiasymbol--get_name.md)|`BSTR`|Name of the typedef.|  
|[IDiaSymbol::get_nested](../../debugger/debug-interface-access/idiasymbol--get_nested.md)|`BOOL`|`TRUE` if this typedef is nested in a lexical scope.|  
|[IDiaSymbol::get_overloadedOperator](../../debugger/debug-interface-access/idiasymbol--get_overloadedoperator.md)|`BOOL`|`TRUE` if this typedef has an overloaded operator.|  
|[IDiaSymbol::get_packed](../../debugger/debug-interface-access/idiasymbol--get_packed.md)|`BOOL`|`TRUE` if this typedef is packed.|  
|[IDiaSymbol::get_reference](../../debugger/debug-interface-access/idiasymbol--get_reference.md)|`BOOL`|`TRUE` if this typedef is a reference.|  
|[IDiaSymbol::get_scoped](../../debugger/debug-interface-access/idiasymbol--get_scoped.md)|`BOOL`|`TRUE` if this typedef is in a nonglobal lexical scope.|  
|[IDiaSymbol::get_symIndexId](../../debugger/debug-interface-access/idiasymbol--get_symindexid.md)|`DWORD`|Index ID of symbol.|  
|[IDiaSymbol::get_symTag](../../debugger/debug-interface-access/idiasymbol--get_symtag.md)|`DWORD`|Returns `SymTagTypedef` (one of the [SymTagEnum Enumeration](../../debugger/debug-interface-access/symtagenum.md) values).|  
|[IDiaSymbol::get_type](../../debugger/debug-interface-access/idiasymbol--get_type.md)|`IDiaSymbol*`|Symbol for the underlying type.|  
|[IDiaSymbol::get_typeId](../../debugger/debug-interface-access/idiasymbol--get_typeid.md)|`DWORD`|ID of the type symbol.|  
|[IDiaSymbol::get_udtKind](../../debugger/debug-interface-access/idiasymbol--get_udtkind.md)|`DWORD`|One of the [UdtKind Enumeration](../../debugger/debug-interface-access/udtkind.md) values.|  
|[IDiaSymbol::get_unalignedType](../../debugger/debug-interface-access/idiasymbol--get_unalignedtype.md)|`BOOL`|`TRUE` if this typedef is not aligned.|  
|[IDiaSymbol::get_virtualTableShape](../../debugger/debug-interface-access/idiasymbol--get_virtualtableshape.md)|`IDiaSymbol*`|The symbol that describes the virtual table shape.|  
|[IDiaSymbol::get_virtualTableShapeId](../../debugger/debug-interface-access/idiasymbol--get_virtualtableshapeid.md)|`DWORD`|ID of the virtual table shape symbol.|  
|[IDiaSymbol::get_volatileType](../../debugger/debug-interface-access/idiasymbol--get_volatiletype.md)|`BOOL`|`TRUE` if this typedef is marked as volatile.|  
  
## Remarks  
 Since a typedef can represent a class, pointer, or user-defined type (UDT), the symbol for a typedef shares the same properties as one of those other types of symbols.  
  
## See Also  
 [Class Hierarchy of Symbol Types](../../debugger/debug-interface-access/class-hierarchy-of-symbol-types.md)