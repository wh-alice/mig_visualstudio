---
title: "IDiaSymbol::get_isMSILNetmodule | hehe"
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
  - "IDiaSymbol::get_isMSILNetmodule method"
ms.assetid: 593827f3-8437-4a12-ada4-ff715ec95fb2
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
# IDiaSymbol::get_isMSILNetmodule
Retrieves a flag indicating whether the module is a .netmodule (a Microsoft Intermediate Language (MSIL) module that contains only metadata and no native symbols).  
  
## Syntax  
  
```cpp#  
HRESULT get_isMSILNetmodule(  
   BOOL *pFlag  
);  
```  
  
#### Parameters  
 `pFlag`  
 [out] Returns `TRUE` if the module is MSIL; otherwise, returns `FALSE`.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE` or an error code.  
  
> [!NOTE]
>  A return value of `S_FALSE` means that the property is not available for the symbol.  
  
## Remarks  
 This property is available from the `SymTagCompilandDetails` symbol type (see [CompilandDetails](../debug-interface-access/compilanddetails.md)).  
  
## Requirements  
  
|Requirement|Description|  
|-----------------|-----------------|  
|Header:|dia2.h|  
|Version:|DIA SDK v8.0|  
  
## See Also  
 [IDiaSymbol](../debug-interface-access/idiasymbol.md)   
 [CompilandDetails](../debug-interface-access/compilanddetails.md)