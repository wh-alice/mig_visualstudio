---
title: "Annotation"
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
  - "SymTabAnnotation symbol"
  - "Annotation symbol"
ms.assetid: eb9f759b-98a5-45fc-b085-91f1f2666e72
caps.latest.revision: 6
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
# Annotation
A location program code can be annotated with a `SymTagAnnotation` symbol.  
  
## Properties  
 The following table shows the properties that are valid for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[IDiaSymbol::get_addressOffset](../VS_debugger/idiasymbol--get_addressoffset.md)|`DWORD`|Offset part of location; for details, see the [LocationType Enumeration](../VS_debugger/locationtype.md).|  
|[IDiaSymbol::get_addressSection](../VS_debugger/idiasymbol--get_addresssection.md)|`DWORD`|Section part of location; for details, see the [LocationType Enumeration](../VS_debugger/locationtype.md).|  
|[IDiaSymbol::get_dataKind](../VS_debugger/idiasymbol--get_datakind.md)|`DWORD`|One of the [DataKind Enumeration](../VS_debugger/datakind.md) values.|  
|[IDiaSymbol::get_relativeVirtualAddress](../VS_debugger/idiasymbol--get_relativevirtualaddress.md)|`DWORD`|Relative position of this annotation within its module.|  
|[IDiaSymbol::get_symIndexId](../VS_debugger/idiasymbol--get_symindexid.md)|`DWORD`|Index ID of symbol.|  
|[IDiaSymbol::get_symTag](../VS_debugger/idiasymbol--get_symtag.md)|`DWORD`|Returns `SymTagAnnotation` (one of the [SymTagEnum Enumeration](../VS_debugger/symtagenum.md) values).|  
|[IDiaSymbol::get_value](../VS_debugger/idiasymbol--get_value.md)|`VARIANT`|The value of constant data.|  
|[IDiaSymbol::get_virtualAddress](../VS_debugger/idiasymbol--get_virtualaddress.md)|`ULONGLONG`|Position of this annotation within the executable image.|  
  
## See Also  
 [Lexical Hierarchy of Symbol Types](../VS_debugger/lexical-hierarchy-of-symbol-types.md)   
 [LocationType Enumeration](../VS_debugger/locationtype.md)   
 [Symbol Locations](../VS_debugger/symbol-locations.md)