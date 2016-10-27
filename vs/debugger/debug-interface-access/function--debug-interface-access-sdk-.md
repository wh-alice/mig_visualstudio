---
title: "Function (Debug Interface Access SDK)"
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
  - "Function symbol"
ms.assetid: 458dc91c-b78b-4427-84f4-615d89e26760
caps.latest.revision: 22
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
# Function (Debug Interface Access SDK)
Each function is identified by a `SymTagFunction` symbol.  
  
## Properties  
 The following table shows the properties that are valid for this symbol type.  
  
|Property|`Data type`|Description|  
|--------------|-----------------|-----------------|  
|[IDiaSymbol::get_access](../../debugger/debug-interface-access/idiasymbol--get_access.md)|`DWORD`|One of the values of the [CV_access_e Enumeration](../../debugger/debug-interface-access/cv_access_e.md), if the function is a member function.|  
|[IDiaSymbol::get_addressOffset](../../debugger/debug-interface-access/idiasymbol--get_addressoffset.md)|`DWORD`|Offset part of location; for details, see the [LocationType Enumeration](../../debugger/debug-interface-access/locationtype.md).|  
|[IDiaSymbol::get_addressSection](../../debugger/debug-interface-access/idiasymbol--get_addresssection.md)|`DWORD`|Section part of location; for details, see the [LocationType Enumeration](../../debugger/debug-interface-access/locationtype.md).|  
|[IDiaSymbol::get_classParent](../../debugger/debug-interface-access/idiasymbol--get_classparent.md)|`IDiaSymbol*`|Symbol for the class, if the function is a member function.|  
|[IDiaSymbol::get_classParentId](../../debugger/debug-interface-access/idiasymbol--get_classparentid.md)|`DWORD`|ID of the class parent symbol.|  
|[IDiaSymbol::get_constType](../../debugger/debug-interface-access/idiasymbol--get_consttype.md)|`BOOL`|`TRUE` if the function is marked as a constant.|  
|[IDiaSymbol::get_customCallingConvention](../../debugger/debug-interface-access/idiasymbol--get_customcallingconvention.md)|`BOOL`|`TRUE` if the function uses a custom calling convention (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_farReturn](../../debugger/debug-interface-access/idiasymbol--get_farreturn.md)|`BOOL`|`TRUE` if the function performs a far return (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_hasAlloca](../../debugger/debug-interface-access/idiasymbol--get_hasalloca.md)|`BOOL`|`TRUE` if the function uses allocated memory function (only uinnder DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_hasEH](../../debugger/debug-interface-access/idiasymbol--get_haseh.md)|`BOOL`|`TRUE` if the function contains C++-style exception handling (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_hasEHa](../../debugger/debug-interface-access/idiasymbol--get_haseha.md)|`BOOL`|`TRUE` if the function contains asynchronous exception handling (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_hasInlAsm](../../debugger/debug-interface-access/idiasymbol--get_hasinlasm.md)|`BOOL`|`TRUE` if the function contains inline assembly (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_hasLongJump](../../debugger/debug-interface-access/idiasymbol--get_haslongjump.md)|`BOOL`|`TRUE` if the function contains a [longjmp](../Topic/longjmp.md) call (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_hasSecurityChecks](../../debugger/debug-interface-access/idiasymbol--get_hassecuritychecks.md)|`BOOL`|`TRUE` if the function contains security checks (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_hasSEH](../../debugger/debug-interface-access/idiasymbol--get_hasseh.md)|`BOOL`|`TRUE` if the function contains Win32-style structured exception handling (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_hasSetJump](../../debugger/debug-interface-access/idiasymbol--get_hassetjump.md)|`BOOL`|`TRUE` if the function contains a [setjmp](../Topic/setjmp.md) call (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_interruptReturn](../../debugger/debug-interface-access/idiasymbol--get_interruptreturn.md)|`BOOL`|`TRUE` if the function has a return from interrupt (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_intro](../../debugger/debug-interface-access/idiasymbol--get_intro.md)|`BOOL`|`TRUE` if a function is intro virtual.|  
|[IDiaSymbol::get_InlSpec](../../debugger/debug-interface-access/idiasymbol--get_inlspec.md)|`BOOL`|`TRUE` if the function has been marked with one of the [inline, __inline, \__forceinline](../../misc/inline--__inline--__forceinline.md) attributes.|  
|[IDiaSymbol::get_isNaked](../../debugger/debug-interface-access/idiasymbol--get_isnaked.md)|`BOOL`|`TRUE` if the function is marked with the [naked](../Topic/naked%20\(C++\).md) attribute (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_isStatic](../../debugger/debug-interface-access/idiasymbol--get_isstatic.md)|`BOOL`|`TRUE` if the function is static (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_length](../../debugger/debug-interface-access/idiasymbol--get_length.md)|`ULONGLONG`|Number of bytes of function code, starting from location.|  
|[IDiaSymbol::get_lexicalParent](../../debugger/debug-interface-access/idiasymbol--get_lexicalparent.md)|`IDiaSymbol*`|Symbol of the enclosing compiland.|  
|[IDiaSymbol::get_lexicalParentId](../../debugger/debug-interface-access/idiasymbol--get_lexicalparentid.md)|`DWORD`|ID of the lexical parent symbol.|  
|[IDiaSymbol::get_locationType](../../debugger/debug-interface-access/idiasymbol--get_locationtype.md)|`DWORD`|Functions can have static or metadata locations; for details, see [Symbol Locations](../../debugger/debug-interface-access/symbol-locations.md).|  
|[IDiaSymbol::get_name](../../debugger/debug-interface-access/idiasymbol--get_name.md)|`BSTR`|Name of the function.|  
|[IDiaSymbol::get_noInline](../../debugger/debug-interface-access/idiasymbol--get_noinline.md)|`BOOL`|`TRUE` if the function is not an inline function (only n DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_notReached](../../debugger/debug-interface-access/idiasymbol--get_notreached.md)|`BOOL`|`TRUE` if the function is not reachable (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_noReturn](../../debugger/debug-interface-access/idiasymbol--get_noreturn.md)|`BOOL`|`TRUE` if the function does not return a value (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_noStackOrdering](../../debugger/debug-interface-access/idiasymbol--get_nostackordering.md)|`BOOL`|`TRUE` if the function was compiled with buffer security checks but no stack ordering could be done.|  
|[IDiaSymbol::get_optimizedCodeDebugInfo](../../debugger/debug-interface-access/idiasymbol--get_optimizedcodedebuginfo.md)|`BOOL`|`TRUE` if the code has debug information for optimized code (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_pure](../../debugger/debug-interface-access/idiasymbol--get_pure.md)|`BOOL`|`TRUE` if function is pure virtual.|  
|[IDiaSymbol::get_relativeVirtualAddress](../../debugger/debug-interface-access/idiasymbol--get_relativevirtualaddress.md)|`DWORD`|Relative position of this function within its module.|  
|[IDiaSymbol::get_symIndexId](../../debugger/debug-interface-access/idiasymbol--get_symindexid.md)|`DWORD`|Index ID of symbol.|  
|[IDiaSymbol::get_symTag](../../debugger/debug-interface-access/idiasymbol--get_symtag.md)|`DWORD`|Returns `SymTagFunction` (one of the [SymTagEnum Enumeration](../../debugger/debug-interface-access/symtagenum.md) values).|  
|[IDiaSymbol::get_token](../../debugger/debug-interface-access/idiasymbol--get_token.md)|`DWORD`|Metadata token for the function.|  
|[IDiaSymbol::get_type](../../debugger/debug-interface-access/idiasymbol--get_type.md)|`IDiaSymbol*`|Symbol for the function signature.|  
|[IDiaSymbol::get_typeId](../../debugger/debug-interface-access/idiasymbol--get_typeid.md)|`DWORD`|ID of the type symbol.|  
|[IDiaSymbol::get_unalignedType](../../debugger/debug-interface-access/idiasymbol--get_unalignedtype.md)|`BOOL`|`TRUE` if the function is unaligned.|  
|[IDiaSymbol::get_undecoratedName](../../debugger/debug-interface-access/idiasymbol--get_undecoratedname.md)|`BSTR`|The undecorated form of the function name (only in DIA SDK v8.0 or later)|  
|[IDiaSymbol::get_undecoratedNameEx](../../debugger/debug-interface-access/idiasymbol--get_undecoratednameex.md)|`BSTR`|Part or all of the undecorated form of the function name (only in DIA SDK v8.0 or later).|  
|[IDiaSymbol::get_virtual](../../debugger/debug-interface-access/idiasymbol--get_virtual.md)|`BOOL`|`TRUE` if a virtual function.|  
|[IDiaSymbol::get_virtualAddress](../../debugger/debug-interface-access/idiasymbol--get_virtualaddress.md)|`ULONGLONG`|Position of this function within the executable image.|  
|[IDiaSymbol::get_virtualBaseOffset](../../debugger/debug-interface-access/idiasymbol--get_virtualbaseoffset.md)|`DWORD`|If a virtual function, then the offset in the virtual function table.|  
|[IDiaSymbol::get_volatileType](../../debugger/debug-interface-access/idiasymbol--get_volatiletype.md)|`BOOL`|`TRUE` if the function is marked as volatile.|  
  
## See Also  
 [CV_access_e Enumeration](../../debugger/debug-interface-access/cv_access_e.md)   
 [Lexical Hierarchy of Symbol Types](../../debugger/debug-interface-access/lexical-hierarchy-of-symbol-types.md)   
 [LocationType Enumeration](../../debugger/debug-interface-access/locationtype.md)   
 [Symbol Locations](../../debugger/debug-interface-access/symbol-locations.md)