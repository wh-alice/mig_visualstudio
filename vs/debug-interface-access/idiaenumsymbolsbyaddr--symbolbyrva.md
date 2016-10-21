---
title: "IDiaEnumSymbolsByAddr::symbolByRVA | hehe"
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
  - "IDiaEnumSymbolsByAddr::symbolByRVA method"
ms.assetid: f7828029-f2ee-4ccd-afac-785adc60a4c8
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
# IDiaEnumSymbolsByAddr::symbolByRVA
Positions the enumerator by performing a lookup by relative virtual address (RVA).  
  
## Syntax  
  
```cpp#  
HRESULT symbolByRVA (   
   DWORD**      relativeVirtualAddress,  
   IDiaSymbol** ppsymbol  
);  
```  
  
#### Parameters  
 relativeVirtualAddress  
 [in] Address relative to start of image.  
  
 ppsymbol  
 [out] Returns an [IDiaSymbol](../debug-interface-access/idiasymbol.md) object representing the symbol found.  
  
## Return Value  
 If successful, returns `S_OK`. Returns `S_FALSE` if the symbol could not be found. Otherwise, returns an error code.  
  
## See Also  
 [IDiaEnumSymbolsByAddr](../debug-interface-access/idiaenumsymbolsbyaddr.md)   
 [IDiaEnumSymbolsByAddr::symbolByVA](../debug-interface-access/idiaenumsymbolsbyaddr--symbolbyva.md)   
 [IDiaSymbol](../debug-interface-access/idiasymbol.md)