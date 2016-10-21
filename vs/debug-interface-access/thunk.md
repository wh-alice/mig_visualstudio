---
title: "Thunk | hehe"
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
Each `thunk` is identified by a `SymTagThunk` tag.  
  
## Properties  
 The following table shows the properties that are valid for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[IDiaSymbol::get_access](../debug-interface-access/idiasymbol--get_access.md)|`DWORD`|Access modifier attribute, one of the [CV_access_e Enumeration](../debug-interface-access/cv_access_e.md) values (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_addressOffset](../debug-interface-access/idiasymbol--get_addressoffset.md)|`DWORD`|Offset part of location; for details, see the [LocationType Enumeration](../debug-interface-access/locationtype.md).|  
|[IDiaSegment::get_addressSection](../debug-interface-access/idiasegment--get_addresssection.md)|`DWORD`|Section part of location; for details, see the [LocationType Enumeration](../debug-interface-access/locationtype.md).|  
|[IDiaSymbol::get_classParent](../debug-interface-access/idiasymbol--get_classparent.md)|`IDiaSymbol*`|Enclosing class parent, if any (only under DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_classParentId](../debug-interface-access/idiasymbol--get_classparentid.md)|`DWORD`|ID of the enclosing class parent symbol (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_constType](../debug-interface-access/idiasymbol--get_consttype.md)|`BOOL`|TRUE if the thunk is marked as constant (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_intro](../debug-interface-access/idiasymbol--get_intro.md)|`BOOL`|TRUE if the thunk is an introduction to a virtual function (only in DIA SDK V8.0 or later)|  
|[IDiaSymbol::get_isStatic](../debug-interface-access/idiasymbol--get_isstatic.md)|`BOOL`|TRUE if the thunk is considered static (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_length](../debug-interface-access/idiasymbol--get_length.md)|`ULONGLONG`|Number of bytes of code in the thunk.|  
|[IDiaSymbol::get_lexicalParent](../debug-interface-access/idiasymbol--get_lexicalparent.md)|`IDiaSymbol*`|Symbol for the enclosing compiland, block, or function.|  
|[IDiaSymbol::get_lexicalParentId](../debug-interface-access/idiasymbol--get_lexicalparentid.md)|`DWORD`|ID of the lexical parent symbol.|  
|[IDiaSymbol::get_locationType](../debug-interface-access/idiasymbol--get_locationtype.md)|`DWORD`|End points have static location; for details, see [Symbol Locations](../debug-interface-access/symbol-locations.md) enumeration.|  
|[IDiaSymbol::get_name](../debug-interface-access/idiasymbol--get_name.md)|`BSTR`|Name of the thunk.|  
|[IDiaSymbol::get_pure](../debug-interface-access/idiasymbol--get_pure.md)|`BOOL`|TRUE if the thunk is purely virtual (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_relativeVirtualAddress](../debug-interface-access/idiasymbol--get_relativevirtualaddress.md)|`DWORD`|Relative position of this thunk within its module.|  
|[IDiaSymbol::get_symIndexId](../debug-interface-access/idiasymbol--get_symindexid.md)|`DWORD`|Index ID of symbol.|  
|[IDiaSymbol::get_symTag](../debug-interface-access/idiasymbol--get_symtag.md)|`DWORD`|Returns `SymTagThunk` (one of the [SymTagEnum Enumeration](../debug-interface-access/symtagenum.md) values).|  
|[IDiaSymbol::get_targetOffset](../debug-interface-access/idiasymbol--get_targetoffset.md)|`DWORD`|Offset part of location of the thunk target.|  
|[IDiaSymbol::get_targetRelativeVirtualAddress](../debug-interface-access/idiasymbol--get_targetrelativevirtualaddress.md)|`DWORD`|Relative virtual address of the thunk target in its enclosing block.|  
|[IDiaSymbol::get_targetSection](../debug-interface-access/idiasymbol--get_targetsection.md)|`DWORD`|Section part of the thunk target.|  
|[IDiaSymbol::get_targetVirtualAddress](../debug-interface-access/idiasymbol--get_targetvirtualaddress.md)|`ULONGLONG`|Position of the thunk target in the executable image.|  
|[IDiaSymbol::get_thunkOrdinal](../debug-interface-access/idiasymbol--get_thunkordinal.md)|`DWORD`|Thunk type, as defined by the [THUNK_ORDINAL Enumeration](../debug-interface-access/thunk_ordinal.md).|  
|[IDiaSymbol::get_type](../debug-interface-access/idiasymbol--get_type.md)|`IDiaSymbol*`|The type of this thunk (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_typeId](../debug-interface-access/idiasymbol--get_typeid.md)|`DWORD`|ID of the type symbol (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_unalignedType](../debug-interface-access/idiasymbol--get_unalignedtype.md)|`BOOL`|`TRUE` if the thunk is not aligned (only in DIA SDK V8.0 or later),|  
|[IDiaSymbol::get_virtual](../debug-interface-access/idiasymbol--get_virtual.md)|`BOOL`|`TRUE` if the thunk is virtual (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_virtualAddress](../debug-interface-access/idiasymbol--get_virtualaddress.md)|`ULONGLONG`|Position of this thunk within the executable image.|  
|[IDiaSymbol::get_virtualBaseOffset](../debug-interface-access/idiasymbol--get_virtualbaseoffset.md)|`DWORD`|The offset in the virtual table to this thunk (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_volatileType](../debug-interface-access/idiasymbol--get_volatiletype.md)|`BOOL`|`TRUE` if the thunk is marked as volatile (only in DIA SDK V8.0 or later).|  
  
## See Also  
 [Lexical Hierarchy of Symbol Types](../debug-interface-access/lexical-hierarchy-of-symbol-types.md)   
 [LocationType Enumeration](../debug-interface-access/locationtype.md)   
 [THUNK_ORDINAL Enumeration](../debug-interface-access/thunk_ordinal.md)