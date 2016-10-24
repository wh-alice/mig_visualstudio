---
title: "FunctionType | testtitle"
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
  - "function signature"
  - "FunctionType symbol"
ms.assetid: 646a07e7-9d4f-4e21-95e3-3e403cdd4843
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
# FunctionType
Each unique function signature is identified by a `SymTagFunctionType` symbol. Each parameter is identified as a class child symbol with a `SymTagFunctionArgType` tag.  
  
## Properties  
 The following table shows additional valid properties for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[IDiaSymbol::get_callingConvention](../debug-interface-access/idiasymbol--get_callingconvention.md)|`DWORD`|One of the values of the [CV_call_e Enumeration](../debug-interface-access/cv_call_e.md).|  
|[IDiaSymbol::get_classParent](../debug-interface-access/idiasymbol--get_classparent.md)|`IDiaSymbol*`|Class that this function (or method) is a member of.|  
|[IDiaSymbol::get_classParentId](../debug-interface-access/idiasymbol--get_classparentid.md)|`DWORD`|ID of the class parent symbol.|  
|[IDiaSymbol::get_constType](../debug-interface-access/idiasymbol--get_consttype.md)|`BOOL`|`TRUE` if the function is marked as constant.|  
|[IDiaSymbol::get_count](../debug-interface-access/idiasymbol--get_count.md)|`DWORD`|Number of function parameters.|  
|[IDiaSymbol::get_lexicalParent](../debug-interface-access/idiasymbol--get_lexicalparent.md)|`IDiaSymbol*`|Symbol of the enclosing compiland.|  
|[IDiaSymbol::get_lexicalParentId](../debug-interface-access/idiasymbol--get_lexicalparentid.md)|`DWORD`|ID of the lexical parent symbol.|  
|[IDiaSymbol::get_objectPointerType](../debug-interface-access/idiasymbol--get_objectpointertype.md)|`IDiaSymbol*`|Type of the method's object pointer ("this").|  
|[IDiaSymbol::get_symIndexId](../debug-interface-access/idiasymbol--get_symindexid.md)|`DWORD`|Index ID of symbol.|  
|[IDiaSymbol::get_symTag](../debug-interface-access/idiasymbol--get_symtag.md)|`DWORD`|Returns `SymTagFunctionType` (one of the [SymTagEnum Enumeration](../debug-interface-access/symtagenum.md) values).|  
|[IDiaSymbol::get_thisAdjust](../debug-interface-access/idiasymbol--get_thisadjust.md)|`LONG`|Logical "this" adjustor for the method.|  
|[IDiaSymbol::get_type](../debug-interface-access/idiasymbol--get_type.md)|`IDiaSymbol*`|Symbol for the return value type.|  
|[IDiaSymbol::get_typeId](../debug-interface-access/idiasymbol--get_typeid.md)|`DWORD`|ID of the type symbol.|  
|[IDiaSymbol::get_unalignedType](../debug-interface-access/idiasymbol--get_unalignedtype.md)|`BOOL`|`TRUE` if the function is unaligned.|  
|[IDiaSymbol::get_volatileType](../debug-interface-access/idiasymbol--get_volatiletype.md)|`BOOL`|`TRUE` if the function is marked as volatile.|  
  
## See Also  
 [Class Hierarchy of Symbol Types](../debug-interface-access/class-hierarchy-of-symbol-types.md)   
 [CV_access_e Enumeration](../debug-interface-access/cv_access_e.md)   
 [FunctionArgType](../debug-interface-access/functionargtype.md)