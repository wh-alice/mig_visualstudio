---
title: "IDiaSession::findLines | hehe"
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
  - "IDiaSession::findLines method"
ms.assetid: d6e84916-fd55-457e-b057-57f97b51fe73
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
# IDiaSession::findLines
Retrieves line numbers within specified compiland and source file identifiers.  
  
## Syntax  
  
```cpp#  
HRESULT findLines (   
   IDiaSymbol*           compiland,  
   IDiaSourceFile*       file,  
   IDiaEnumLineNumbers** ppResult  
);  
```  
  
#### Parameters  
 `compiland`  
 [in]An [IDiaSymbol](../debug-interface-access/idiasymbol.md) object representing the compiland. Use this interface as a context in which to search for the line numbers.  
  
 `file`  
 [in] An [IDiaSourceFile](../debug-interface-access/idiasourcefile.md) object representing the source file in which to search for the line numbers.  
  
 `ppResult`  
 [out] Returns an [IDiaEnumLineNumbers](../debug-interface-access/idiaenumlinenumbers.md) object that contains a list of the line numbers retrieved.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDiaEnumLineNumbers](../debug-interface-access/idiaenumlinenumbers.md)   
 [IDiaSession](../debug-interface-access/idiasession.md)   
 [IDiaSourceFile](../debug-interface-access/idiasourcefile.md)   
 [IDiaSymbol](../debug-interface-access/idiasymbol.md)