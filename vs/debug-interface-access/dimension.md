---
title: "Dimension | testtitle"
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
  - "Dimension Symbol"
ms.assetid: 94f791da-bfea-454f-8a14-da31e8e1596a
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
# Dimension
Each FORTRAN array has a dimension that is identified by a `SymTagDimension` symbol.  
  
## Properties  
 The following table shows additional valid properties for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[IDiaSymbol::get_lowerBound](../debug-interface-access/idiasymbol--get_lowerbound.md)|`IDiaSymbol*`|Lower bound of a FORTRAN array dimension.|  
|[IDiaSymbol::get_lowerBoundId](../debug-interface-access/idiasymbol--get_lowerboundid.md)|`DWORD`|ID of the lower-bound symbol.|  
|[IDiaSymbol::get_symIndexId](../debug-interface-access/idiasymbol--get_symindexid.md)|`DWORD`|Index ID of symbol.|  
|[IDiaSymbol::get_symTag](../debug-interface-access/idiasymbol--get_symtag.md)|`DWORD`|Returns `SymTagDimension` (one of the [SymTagEnum Enumeration](../debug-interface-access/symtagenum.md) values).|  
|[IDiaSymbol::get_upperBound](../debug-interface-access/idiasymbol--get_upperbound.md)|`IDiaSymbol*`|Upper bound of a FORTRAN array dimension.|  
|[IDiaSymbol::get_upperBoundId](../debug-interface-access/idiasymbol--get_upperboundid.md)|`DWORD`|ID of the upper-bound symbol.|  
  
## See Also  
 [ArrayType](../debug-interface-access/arraytype.md)   
 [Class Hierarchy of Symbol Types](../debug-interface-access/class-hierarchy-of-symbol-types.md)