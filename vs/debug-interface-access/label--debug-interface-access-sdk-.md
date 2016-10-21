---
title: "Label (Debug Interface Access SDK)"
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
  - "locations, in program code"
  - "Label symbol"
ms.assetid: 8cef7620-5bc8-4500-8bd0-e9e638bccb24
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
# Label (Debug Interface Access SDK)
A location in program code is identified by a `SymTagLabel` symbol.  
  
## Properties  
 The following table shows the properties that are valid for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[IDiaSymbol::get_addressOffset](../debug-interface-access/idiasymbol--get_addressoffset.md)|`DWORD`|Offset part of location; for details, see the [LocationType Enumeration](../debug-interface-access/locationtype.md).|  
|[IDiaSymbol::get_addressSection](../debug-interface-access/idiasymbol--get_addresssection.md)|`DWORD`|Section part of location; for details, see the [LocationType Enumeration](../debug-interface-access/locationtype.md).|  
|[IDiaSymbol::get_customCallingConvention](../debug-interface-access/idiasymbol--get_customcallingconvention.md)|`BOOL`|`TRUE` if the label uses a custom calling convention.|  
|[IDiaSymbol::get_farReturn](../debug-interface-access/idiasymbol--get_farreturn.md)|`BOOL`|`TRUE` if label performs a far return.|  
|[IDiaSymbol::get_interruptReturn](../debug-interface-access/idiasymbol--get_interruptreturn.md)|`BOOL`|`TRUE` if label contains a return from interrupt.|  
|[IDiaSymbol::get_lexicalParent](../debug-interface-access/idiasymbol--get_lexicalparent.md)|`IDiaSymbol*`|Symbol for the enclosing compiland, block, or function.|  
|[IDiaSymbol::get_lexicalParentId](../debug-interface-access/idiasymbol--get_lexicalparentid.md)|`DWORD`|ID of the lexical parent symbol.|  
|[IDiaSymbol::get_locationType](../debug-interface-access/idiasymbol--get_locationtype.md)|`DWORD`|Labels have static locations; for details, see the [Symbol Locations](../debug-interface-access/symbol-locations.md) enumeration.|  
|[IDiaSymbol::get_name](../debug-interface-access/idiasymbol--get_name.md)|`BSTR`|The label's name.|  
|[IDiaSymbol::get_noInline](../debug-interface-access/idiasymbol--get_noinline.md)|`BOOL`|`TRUE` if the label was specified with the [noinline](../Topic/noinline.md) attribute.|  
|[IDiaSymbol::get_noReturn](../debug-interface-access/idiasymbol--get_noreturn.md)|`BOOL`|`TRUE` if the label was specified with the [noreturn](../Topic/noreturn.md) attribute.|  
|[IDiaSymbol::get_notReached](../debug-interface-access/idiasymbol--get_notreached.md)|`BOOL`|`TRUE` if the label is never called.|  
|[IDiaSymbol::get_offset](../debug-interface-access/idiasymbol--get_offset.md)|`LONG`|Offset of symbol in memory; for details, see the [LocationType Enumeration](../debug-interface-access/locationtype.md), `LocIsRegRel`.|  
|[IDiaSymbol::get_optimizedCodeDebugInfo](../debug-interface-access/idiasymbol--get_optimizedcodedebuginfo.md)|`BOOL`|`TRUE` if the code has debug information for optimized code.|  
|[IDiaSymbol::get_relativeVirtualAddress](../debug-interface-access/idiasymbol--get_relativevirtualaddress.md)|`DWORD`|Relative position of this label within its module.|  
|[IDiaSymbol::get_symIndexId](../debug-interface-access/idiasymbol--get_symindexid.md)|`DWORD`|Index ID of symbol.|  
|[IDiaSymbol::get_symTag](../debug-interface-access/idiasymbol--get_symtag.md)|`DWORD`|Returns `SymTagFuncDebugLabel` (one of the [SymTagEnum Enumeration](../debug-interface-access/symtagenum.md) values).|  
|[IDiaSymbol::get_virtualAddress](../debug-interface-access/idiasymbol--get_virtualaddress.md)|`ULONGLONG`|Position of this label within the executable image.|  
  
## See Also  
 [Lexical Hierarchy of Symbol Types](../debug-interface-access/lexical-hierarchy-of-symbol-types.md)   
 [LocationType Enumeration](../debug-interface-access/locationtype.md)   
 [Symbol Locations](../debug-interface-access/symbol-locations.md)