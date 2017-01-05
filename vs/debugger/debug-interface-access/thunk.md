---
title: "Thunk"
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
  - "thunk properties [DIA SDK]"
  - "thunk symbol"
ms.assetid: 01abb95f-d89a-465c-a4eb-8e8509598c95
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
# Thunk
[!INCLUDE[vs2017banner](../../code-quality/includes/vs2017banner.md)]

Each `thunk` is identified by a `SymTagThunk` tag.  
  
## Properties  
 The following table shows the properties that are valid for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[IDiaSymbol::get_access](../../debugger/debug-interface-access/idiasymbol--get_access.md)|`DWORD`|Access modifier attribute, one of the [CV_access_e Enumeration](../../debugger/debug-interface-access/cv_access_e.md) values (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_addressOffset](../../debugger/debug-interface-access/idiasymbol--get_addressoffset.md)|`DWORD`|Offset part of location; for details, see the [LocationType Enumeration](../../debugger/debug-interface-access/locationtype.md).|  
|[IDiaSegment::get_addressSection](../../debugger/debug-interface-access/idiasegment--get_addresssection.md)|`DWORD`|Section part of location; for details, see the [LocationType Enumeration](../../debugger/debug-interface-access/locationtype.md).|  
|[IDiaSymbol::get_classParent](../../debugger/debug-interface-access/idiasymbol--get_classparent.md)|`IDiaSymbol*`|Enclosing class parent, if any (only under DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_classParentId](../../debugger/debug-interface-access/idiasymbol--get_classparentid.md)|`DWORD`|ID of the enclosing class parent symbol (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_constType](../../debugger/debug-interface-access/idiasymbol--get_consttype.md)|`BOOL`|TRUE if the thunk is marked as constant (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_intro](../../debugger/debug-interface-access/idiasymbol--get_intro.md)|`BOOL`|TRUE if the thunk is an introduction to a virtual function (only in DIA SDK V8.0 or later)|  
|[IDiaSymbol::get_isStatic](../../debugger/debug-interface-access/idiasymbol--get_isstatic.md)|`BOOL`|TRUE if the thunk is considered static (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_length](../../debugger/debug-interface-access/idiasymbol--get_length.md)|`ULONGLONG`|Number of bytes of code in the thunk.|  
|[IDiaSymbol::get_lexicalParent](../../debugger/debug-interface-access/idiasymbol--get_lexicalparent.md)|`IDiaSymbol*`|Symbol for the enclosing compiland, block, or function.|  
|[IDiaSymbol::get_lexicalParentId](../../debugger/debug-interface-access/idiasymbol--get_lexicalparentid.md)|`DWORD`|ID of the lexical parent symbol.|  
|[IDiaSymbol::get_locationType](../../debugger/debug-interface-access/idiasymbol--get_locationtype.md)|`DWORD`|End points have static location; for details, see [Symbol Locations](../../debugger/debug-interface-access/symbol-locations.md) enumeration.|  
|[IDiaSymbol::get_name](../../debugger/debug-interface-access/idiasymbol--get_name.md)|`BSTR`|Name of the thunk.|  
|[IDiaSymbol::get_pure](../../debugger/debug-interface-access/idiasymbol--get_pure.md)|`BOOL`|TRUE if the thunk is purely virtual (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_relativeVirtualAddress](../../debugger/debug-interface-access/idiasymbol--get_relativevirtualaddress.md)|`DWORD`|Relative position of this thunk within its module.|  
|[IDiaSymbol::get_symIndexId](../../debugger/debug-interface-access/idiasymbol--get_symindexid.md)|`DWORD`|Index ID of symbol.|  
|[IDiaSymbol::get_symTag](../../debugger/debug-interface-access/idiasymbol--get_symtag.md)|`DWORD`|Returns `SymTagThunk` (one of the [SymTagEnum Enumeration](../../debugger/debug-interface-access/symtagenum.md) values).|  
|[IDiaSymbol::get_targetOffset](../../debugger/debug-interface-access/idiasymbol--get_targetoffset.md)|`DWORD`|Offset part of location of the thunk target.|  
|[IDiaSymbol::get_targetRelativeVirtualAddress](../../debugger/debug-interface-access/idiasymbol--get_targetrelativevirtualaddress.md)|`DWORD`|Relative virtual address of the thunk target in its enclosing block.|  
|[IDiaSymbol::get_targetSection](../../debugger/debug-interface-access/idiasymbol--get_targetsection.md)|`DWORD`|Section part of the thunk target.|  
|[IDiaSymbol::get_targetVirtualAddress](../../debugger/debug-interface-access/idiasymbol--get_targetvirtualaddress.md)|`ULONGLONG`|Position of the thunk target in the executable image.|  
|[IDiaSymbol::get_thunkOrdinal](../../debugger/debug-interface-access/idiasymbol--get_thunkordinal.md)|`DWORD`|Thunk type, as defined by the [THUNK_ORDINAL Enumeration](../../debugger/debug-interface-access/thunk_ordinal.md).|  
|[IDiaSymbol::get_type](../../debugger/debug-interface-access/idiasymbol--get_type.md)|`IDiaSymbol*`|The type of this thunk (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_typeId](../../debugger/debug-interface-access/idiasymbol--get_typeid.md)|`DWORD`|ID of the type symbol (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_unalignedType](../../debugger/debug-interface-access/idiasymbol--get_unalignedtype.md)|`BOOL`|`TRUE` if the thunk is not aligned (only in DIA SDK V8.0 or later),|  
|[IDiaSymbol::get_virtual](../../debugger/debug-interface-access/idiasymbol--get_virtual.md)|`BOOL`|`TRUE` if the thunk is virtual (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_virtualAddress](../../debugger/debug-interface-access/idiasymbol--get_virtualaddress.md)|`ULONGLONG`|Position of this thunk within the executable image.|  
|[IDiaSymbol::get_virtualBaseOffset](../../debugger/debug-interface-access/idiasymbol--get_virtualbaseoffset.md)|`DWORD`|The offset in the virtual table to this thunk (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_volatileType](../../debugger/debug-interface-access/idiasymbol--get_volatiletype.md)|`BOOL`|`TRUE` if the thunk is marked as volatile (only in DIA SDK V8.0 or later).|  
  
## See Also  
 [Lexical Hierarchy of Symbol Types](../../debugger/debug-interface-access/lexical-hierarchy-of-symbol-types.md)   
 [LocationType Enumeration](../../debugger/debug-interface-access/locationtype.md)   
 [THUNK_ORDINAL Enumeration](../../debugger/debug-interface-access/thunk_ordinal.md)