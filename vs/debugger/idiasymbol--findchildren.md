---
title: "IDiaSymbol::findChildren"
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
  - "IDiaSymbol::findChildren method"
ms.assetid: 5fe7573a-e48b-428d-9c17-7421b7209246
caps.latest.revision: 12
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
# IDiaSymbol::findChildren
Retrieves the children of the symbol.  
  
## Syntax  
  
```cpp#  
HRESULT findChildren (   
   enum SymTagEnum   symtag,  
   LPCOLESTR         name,  
   DWORD             compareFlags,  
   IDiaEnumSymbols** ppResult  
);  
```  
  
#### Parameters  
 `symtag`  
 [in] Specifies the symbol tags of the children to be retrieved, as defined in the [SymTagEnum Enumeration](../debugger/symtagenum.md). Set to `SymTagNull` for all children to be retrieved.  
  
 `name`  
 [in] Specifies the name of the children to be retrieved. Set to `NULL` for all children to be retrieved.  
  
 `compareFlags`  
 [in] Specifies the comparison options applied to name matching. Values from the [NameSearchOptions Enumeration](../debugger/namesearchoptions.md) enumeration can be used alone or in combination.  
  
 `ppResult`  
 [out] Returns an [IDiaEnumSymbols](../debugger/idiaenumsymbols.md) object that contains a list of the child symbols retrieved.  
  
## Return Value  
 Returns `S_OK` if at least one child of the symbol was found, or returns `S_FALSE` if no children were found; otherwise returns an error code.  
  
## Remarks  
 This method is identical to calling the [IDiaSession::findChildren](../debugger/idiasession--findchildren.md) method with this symbol as the first parameter.  
  
## See Also  
 [IDiaSymbol](../debugger/idiasymbol.md)   
 [SymTagEnum Enumeration](../debugger/symtagenum.md)   
 [IDiaEnumSymbols](../debugger/idiaenumsymbols.md)   
 [IDiaSession::findChildren](../debugger/idiasession--findchildren.md)   
 [NameSearchOptions Enumeration](../debugger/namesearchoptions.md)