---
title: "IDiaSession::findSymbolsByRVAForAcceleratorPointerTag | testtitle"
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
ms.assetid: a073cc45-0c7b-417e-b5fc-a3b08beccdbc
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
# IDiaSession::findSymbolsByRVAForAcceleratorPointerTag
Given a corresponding tag value, this method returns an enumeration of symbols that are contained in a specified parent Accelerator stub function at a specified relative virtual address.  
  
## Syntax  
  
```cpp#  
HRESULT findSymbolsByRVAForAcceleratorPointerTag (   
   IDiaSymbol*           parent,  
   DWORD                 tagValue,  
   DWORD                 rva,  
   IDiaEnumSymbols**     ppResult  
);  
```  
  
#### Parameters  
 `parent`  
 [in] An `IDiaSymbol` that corresponds to the Accelerator stub function to be searched.  
  
 `tagValue`  
 [in] The pointer tag value.  
  
 `rva`  
 [in] The relative virtual address.  
  
 `ppResult`  
 [out] A pointer to an `IDiaEnumSymbols` interface pointer that is initialized with the result.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 Call this method only on an `IDiaSymbol` interface that corresponds to an Accelerator stub function.  
  
## See Also  
 [IDiaSession](../debug-interface-access/idiasession.md)   
 [IDiaEnumSymbols](../debug-interface-access/idiaenumsymbols.md)   
 [IDiaSymbol](../debug-interface-access/idiasymbol.md)