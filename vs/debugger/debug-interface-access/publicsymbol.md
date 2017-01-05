---
title: "PublicSymbol"
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
  - "data symbols [C++]"
  - "PublicSymbol symbol"
  - "global functions [C++], as public symbols"
ms.assetid: f8d33007-302d-4549-9dad-47fb33ea60b7
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
# PublicSymbol
[!INCLUDE[vs2017banner](../../code-quality/includes/vs2017banner.md)]

When the .exe file is created, each public symbol (at a minimum, each global function and data symbol) is given a `SymTagPublicSymbol` tag.  
  
## Properties  
 The following table shows the properties that are valid for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[IDiaSymbol::get_addressOffset](../../debugger/debug-interface-access/idiasymbol--get_addressoffset.md)|`DWORD`|Offset part of location; for details, see the [LocationType Enumeration](../../debugger/debug-interface-access/locationtype.md).|  
|[IDiaSymbol::get_addressSection](../../debugger/debug-interface-access/idiasymbol--get_addresssection.md)|`DWORD`|Section part of location; for details, see the [LocationType Enumeration](../../debugger/debug-interface-access/locationtype.md).|  
|[IDiaSymbol::get_code](../../debugger/debug-interface-access/idiasymbol--get_code.md)|`BOOL`|`TRUE` if the symbol's location is in code.|  
|[IDiaSymbol::get_function](../../debugger/debug-interface-access/idiasymbol--get_function.md)|`BOOL`|`TRUE` if the symbol is a function.|  
|[IDiaSymbol::get_length](../../debugger/debug-interface-access/idiasymbol--get_length.md)|`ULONGLONG`|Length of this symbol in bytes.|  
|[IDiaSymbol::get_lexicalParent](../../debugger/debug-interface-access/idiasymbol--get_lexicalparent.md)|`IDiaSymbol*`|Symbol for the global scope.|  
|[IDiaSymbol::get_lexicalParentId](../../debugger/debug-interface-access/idiasymbol--get_lexicalparentid.md)|`DWORD`|ID of the lexical parent symbol.|  
|[IDiaSymbol::get_locationType](../../debugger/debug-interface-access/idiasymbol--get_locationtype.md)|`DWORD`|Public symbols have static locations; for details, see [Symbol Locations](../../debugger/debug-interface-access/symbol-locations.md).|  
|[IDiaSymbol::get_managed](../../debugger/debug-interface-access/idiasymbol--get_managed.md)|`BOOL`|`TRUE` if the symbol's location is in managed code.|  
|[IDiaSymbol::get_msil](../../debugger/debug-interface-access/idiasymbol--get_msil.md)|`BOOL`|`TRUE` if the symbol's location is in Microsoft Intermediate Language (MSIL) code.|  
|[IDiaSymbol::get_name](../../debugger/debug-interface-access/idiasymbol--get_name.md)|`BSTR`|The fully decorated name of the symbol.|  
|[IDiaSymbol::get_symIndexId](../../debugger/debug-interface-access/idiasymbol--get_symindexid.md)|`DWORD`|Index ID of symbol.|  
|[IDiaSymbol::get_relativeVirtualAddress](../../debugger/debug-interface-access/idiasymbol--get_relativevirtualaddress.md)|`DWORD`|Relative position of the symbol within its block.|  
|[IDiaSymbol::get_symTag](../../debugger/debug-interface-access/idiasymbol--get_symtag.md)|`DWORD`|Returns `SymTagPublicSymbol` (one of the [SymTagEnum Enumeration](../../debugger/debug-interface-access/symtagenum.md) values).|  
|[IDiaSymbol::get_undecoratedName](../../debugger/debug-interface-access/idiasymbol--get_undecoratedname.md)|`BSTR`|The undecorated symbol name.|  
|[IDiaSymbol::get_undecoratedNameEx](../../debugger/debug-interface-access/idiasymbol--get_undecoratednameex.md)|`BSTR`|Part or all of the undecorated symbol name.|  
  
## See Also  
 [Lexical Hierarchy of Symbol Types](../../debugger/debug-interface-access/lexical-hierarchy-of-symbol-types.md)   
 [LocationType Enumeration](../../debugger/debug-interface-access/locationtype.md)   
 [Symbol Locations](../../debugger/debug-interface-access/symbol-locations.md)