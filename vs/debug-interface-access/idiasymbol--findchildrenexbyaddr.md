---
title: "IDiaSymbol::findChildrenExByAddr | hehe"
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
  - "IDiaSymbol::findChildrenExByAddr"
ms.assetid: c1e7885d-2d15-4529-9ac2-32dd22efe31c
caps.latest.revision: 8
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
# IDiaSymbol::findChildrenExByAddr
Retrieves the children of the symbol that are valid at a specified address.  
  
## Syntax  
  
```cpp#  
HRESULT findChildrenExByAddr (   
   enum SymTagEnum   symtag,  
   LPCOLESTR         name,  
   DWORD             compareFlags,  
   DWORD             address,  
   IDiaEnumSymbols** ppResult  
);  
```  
  
#### Parameters  
 `symtag`  
 [in] Specifies the symbol tags of the children to be retrieved, as defined in the [SymTagEnum Enumeration](../debug-interface-access/symtagenum.md). Set to `SymTagNull` for all children to be retrieved.  
  
 `name`  
 [in] Specifies the name of the children to be retrieved. Set to `NULL` for all children to be retrieved.  
  
 `compareFlags`  
 [in] Specifies the comparison options to be applied to name matching. Values from the [NameSearchOptions Enumeration](../debug-interface-access/namesearchoptions.md) enumeration can be used alone or in combination.  
  
 `address`  
 [in] The address of the symbol.  
  
 `ppResult`  
 [out] Returns an [IDiaEnumSymbols](../debug-interface-access/idiaenumsymbols.md) object that contains a list of the child symbols retrieved.  
  
## Return Value  
 Returns `S_OK` if at least one child of the symbol was found, or returns `S_FALSE` if no children were found; otherwise, returns an error code.  
  
## Remarks  
 The local symbols that are returned include live range information.  
  
## Requirements  
 Header: Dia2.h  
  
 Library: diaguids.lib  
  
 DLL: msdia100.dll  
  
## See Also  
 [IDiaSymbol](../debug-interface-access/idiasymbol.md)   
 [SymTagEnum Enumeration](../debug-interface-access/symtagenum.md)   
 [IDiaEnumSymbols](../debug-interface-access/idiaenumsymbols.md)   
 [IDiaSession::findChildren](../debug-interface-access/idiasession--findchildren.md)   
 [NameSearchOptions Enumeration](../debug-interface-access/namesearchoptions.md)