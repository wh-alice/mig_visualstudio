---
title: "ArrayType"
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
  - "ArrayType symbol"
ms.assetid: 1d973a3a-2bde-46df-8625-85d519bb3cc9
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
# ArrayType
An array is identified by a `SymTagArray` symbol.  
  
## Properties  
 The following table shows additional valid properties for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[IDiaSymbol::get_arrayIndexType](../debug-interface-access/idiasymbol--get_arrayindextype.md)|`IDiaSymbol*`|Symbol for the array index type.|  
|[IDiaSymbol::get_arrayIndexTypeId](../debug-interface-access/idiasymbol--get_arrayindextypeid.md)|`DWORD`|ID of the array index type symbol.|  
|[IDiaSymbol::get_constType](../debug-interface-access/idiasymbol--get_consttype.md)|`BOOL`|`TRUE` if the array is marked as const.|  
|[IDiaSymbol::get_count](../debug-interface-access/idiasymbol--get_count.md)|`DWORD`|Number of items in the array.|  
|[IDiaSymbol::get_length](../debug-interface-access/idiasymbol--get_length.md)|`LONGLONG`|Size, in bytes, of this array.|  
|[IDiaSymbol::get_lexicalParent](../debug-interface-access/idiasymbol--get_lexicalparent.md)|`IDiaSymbol*`|Symbol of the enclosing compiland.|  
|[IDiaSymbol::get_lexicalParentId](../debug-interface-access/idiasymbol--get_lexicalparentid.md)|`DWORD`|ID of the lexical parent symbol.|  
|[IDiaSymbol::get_rank](../debug-interface-access/idiasymbol--get_rank.md)|`DWORD`|Rank of a FORTRAN multidimensional array.|  
|[IDiaSymbol::get_symIndexId](../debug-interface-access/idiasymbol--get_symindexid.md)|`DWORD`|Index ID of symbol.|  
|[IDiaSymbol::get_symTag](../debug-interface-access/idiasymbol--get_symtag.md)|`DWORD`|Returns `SymTagArray` (one of the [SymTagEnum Enumeration](../debug-interface-access/symtagenum.md) values).|  
|[IDiaSymbol::get_type](../debug-interface-access/idiasymbol--get_type.md)|`IDiaSymbol*`|Symbol for the array element type.|  
|[IDiaSymbol::get_typeId](../debug-interface-access/idiasymbol--get_typeid.md)|`DWORD`|ID of the array element type symbol.|  
|[IDiaSymbol::get_unalignedType](../debug-interface-access/idiasymbol--get_unalignedtype.md)|`BOOL`|`TRUE` if the array is unaligned|  
|[IDiaSymbol::get_volatileType](../debug-interface-access/idiasymbol--get_volatiletype.md)|`BOOL`|`TRUE` if the array is marked as volatile.|  
  
## See Also  
 [Class Hierarchy of Symbol Types](../debug-interface-access/class-hierarchy-of-symbol-types.md)   
 [Dimension](../debug-interface-access/dimension.md)