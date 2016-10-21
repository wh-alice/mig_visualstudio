---
title: "FuncDebugStart | hehe"
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
  - "FuncDebugStart symbol"
  - "debugging [DIA SDK], start point"
ms.assetid: 1cbc6ca5-87d0-4c30-a39e-0a9dc62ce1a9
caps.latest.revision: 18
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
# FuncDebugStart
If a function has a defined point at which debugging is to begin, that point is identified by a symbol with a `SymTagFuncDebugStart` tag.  
  
## Properties  
 The following table shows the properties that are valid for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[IDiaSymbol::get_addressOffset](../debug-interface-access/idiasymbol--get_addressoffset.md)|`DWORD`|Offset part of location; for details, see the [LocationType Enumeration](../debug-interface-access/locationtype.md).|  
|[IDiaSymbol::get_addressSection](../debug-interface-access/idiasymbol--get_addresssection.md)|`DWORD`|Section part of location; for details, see the [LocationType Enumeration](../debug-interface-access/locationtype.md).|  
|[IDiaSymbol::get_customCallingConvention](../debug-interface-access/idiasymbol--get_customcallingconvention.md)|`BOOL`|`TRUE` if the function uses a custom calling convention (only in DIA SDK v8.0 or later).|  
|[IDiaSymbol::get_farReturn](../debug-interface-access/idiasymbol--get_farreturn.md)|`BOOL`|`TRUE` if function performs a far return (only in DIA SDK v8.0 or later).|  
|[IDiaSymbol::get_interruptReturn](../debug-interface-access/idiasymbol--get_interruptreturn.md)|`BOOL`|`TRUE` if function contains a return from interrupt (only in DIA SDK v8.0 or later).|  
|[IDiaSymbol::get_isStatic](../debug-interface-access/idiasymbol--get_isstatic.md)|`BOOL`|`TRUE` if function is marked as static (only in DIA SDK v8.0 or later).|  
|[IDiaSymbol::get_lexicalParent](../debug-interface-access/idiasymbol--get_lexicalparent.md)|`IDiaSymbol*`|Symbol for the enclosing function.|  
|[IDiaSymbol::get_lexicalParentId](../debug-interface-access/idiasymbol--get_lexicalparentid.md)|`DWORD`|ID of the lexical parent symbol.|  
|[IDiaSymbol::get_locationType](../debug-interface-access/idiasymbol--get_locationtype.md)|`DWORD`|Start points have static locations; for details, see [Symbol Locations](../debug-interface-access/symbol-locations.md).|  
|[IDiaSymbol::get_noInline](../debug-interface-access/idiasymbol--get_noinline.md)|`BOOL`|`TRUE` if the function was specified with the [noinline](../Topic/noinline.md) attribute (only in DIA SDK v8.0 or later).|  
|[IDiaSymbol::get_noReturn](../debug-interface-access/idiasymbol--get_noreturn.md)|`BOOL`|`TRUE` if the function was specified with the [noreturn](../Topic/noreturn.md) attribute (only in DIA SDK v8.0 or later).|  
|[IDiaSymbol::get_notReached](../debug-interface-access/idiasymbol--get_notreached.md)|`BOOL`|`TRUE` if the function is never called (only in DIA SDK v8.0 or later).|  
|[IDiaSymbol::get_offset](../debug-interface-access/idiasymbol--get_offset.md)|`LONG`|Offset of symbol in memory; for details, see the [LocationType Enumeration](../debug-interface-access/locationtype.md), `LocIsRegRel`.|  
|[IDiaSymbol::get_optimizedCodeDebugInfo](../debug-interface-access/idiasymbol--get_optimizedcodedebuginfo.md)|`BOOL`|`TRUE` if the code has debug information for optimized code (only in DIA SDK v8.0 or later).|  
|[IDiaSymbol::get_relativeVirtualAddress](../debug-interface-access/idiasymbol--get_relativevirtualaddress.md)|`DWORD`|Relative position of the function within its block.|  
|[IDiaSymbol::get_symIndexId](../debug-interface-access/idiasymbol--get_symindexid.md)|`DWORD`|Index ID of symbol.|  
|[IDiaSymbol::get_symTag](../debug-interface-access/idiasymbol--get_symtag.md)|`DWORD`|Returns `SymTagFuncDebugStart` (one of the [SymTagEnum Enumeration](../debug-interface-access/symtagenum.md) values).|  
|[IDiaSymbol::get_virtualAddress](../debug-interface-access/idiasymbol--get_virtualaddress.md)|`ULONGLONG`|Position of the function within the executable.|  
  
## See Also  
 [Lexical Hierarchy of Symbol Types](../debug-interface-access/lexical-hierarchy-of-symbol-types.md)   
 [LocationType Enumeration](../debug-interface-access/locationtype.md)   
 [Symbol Locations](../debug-interface-access/symbol-locations.md)