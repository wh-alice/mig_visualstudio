---
title: "IDiaSymbol::findInlineeLinesByAddr | hehe"
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
ms.assetid: f1ab47ca-c851-48ea-9c12-47fb80b31102
caps.latest.revision: 3
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
# IDiaSymbol::findInlineeLinesByAddr
Retrieves an enumeration that allows a client to iterate through the line number information of all functions that are inlined, directly or indirectly, in this symbol within the specified address range.  
  
## Syntax  
  
```cpp#  
HRESULT findInlineeLinesByAddr (   
   DWORD                 isect,  
   DWORD                 offset,  
   DWORD                 length,  
   IDiaEnumLineNumbers** ppResult  
);  
```  
  
#### Parameters  
 `isect`  
 [in] Specifies the section component of the address.  
  
 `offset`  
 [in] Specifies the offset component of the address.  
  
 `length`  
 [in] Specifies the address range, in number of bytes, to cover with this query.  
  
 `ppResult`  
 [out] Holds an `IDiaEnumLineNumbers` object that contains the list of line numbers that are retrieved.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDiaSession](../debug-interface-access/idiasession.md)   
 [IDiaSymbol](../debug-interface-access/idiasymbol.md)   
 [SymTagEnum Enumeration](../debug-interface-access/symtagenum.md)   
 [IDiaEnumLineNumbers](../debug-interface-access/idiaenumlinenumbers.md)   
 [IDiaSession::findInlineeLines](../debug-interface-access/idiasession--findinlineelines.md)