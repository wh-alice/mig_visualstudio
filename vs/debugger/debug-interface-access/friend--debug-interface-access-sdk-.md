---
title: "Friend (Debug Interface Access SDK)"
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
  - "friend functions [DIA SDK]"
  - "friend classes [DIA SDK]"
  - "Friend symbol"
ms.assetid: 5147a170-41ce-4727-8ace-c318e8d11647
caps.latest.revision: 16
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
# Friend (Debug Interface Access SDK)
[!INCLUDE[vs2017banner](../../code-quality/includes/vs2017banner.md)]

Friend classes and friend functions are identified by `SymTagFriend` symbols. They are children of parent user-defined types (UDTs) and have a [IDiaSymbol::get_classParent](../../debugger/debug-interface-access/idiasymbol--get_classparent.md) property.  
  
## Properties  
 The following table shows additional valid properties for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[IDiaSymbol::get_classParent](../../debugger/debug-interface-access/idiasymbol--get_classparent.md)|`IDiaSymbol*`|Symbol for the UDT parent.|  
|[IDiaSymbol::get_classParentId](../../debugger/debug-interface-access/idiasymbol--get_classparentid.md)|`DWORD`|ID of the class parent symbol.|  
|[IDiaSymbol::get_name](../../debugger/debug-interface-access/idiasymbol--get_name.md)|`BSTR`|Name of the class or function.|  
|[IDiaSymbol::get_symIndexId](../../debugger/debug-interface-access/idiasymbol--get_symindexid.md)|`DWORD`|Index ID of symbol.|  
|[IDiaSymbol::get_symTag](../../debugger/debug-interface-access/idiasymbol--get_symtag.md)|`DWORD`|Returns `SymTagFriend` (one of the [SymTagEnum Enumeration](../../debugger/debug-interface-access/symtagenum.md) values).|  
|[IDiaSymbol::get_type](../../debugger/debug-interface-access/idiasymbol--get_type.md)|`IDiaSymbol*`|Symbol for the class or function.|  
|[IDiaSymbol::get_typeId](../../debugger/debug-interface-access/idiasymbol--get_typeid.md)|`DWORD`|ID of the type symbol.|  
  
## See Also  
 [Class Hierarchy of Symbol Types](../../debugger/debug-interface-access/class-hierarchy-of-symbol-types.md)