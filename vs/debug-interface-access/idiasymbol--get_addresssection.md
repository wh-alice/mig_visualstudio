---
title: "IDiaSymbol::get_addressSection | testtitle"
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
  - "IDiaSymbol::get_addressSection method"
ms.assetid: fe80d479-3bb5-4f55-9b62-1bd58d0a60ce
caps.latest.revision: 9
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
# IDiaSymbol::get_addressSection
Retrieves the section part of an address location. Use when the [LocationType Enumeration](../debug-interface-access/locationtype.md) is set to `LocIsStatic`.  
  
## Syntax  
  
```cpp#  
HRESULT get_addressSection (   
   DWORD* pRetVal  
);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] Returns the section part of an address location.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE` or an error code.  
  
> [!NOTE]
>  A return value of `S_FALSE` means that the property is not available for the symbol.  
  
## Remarks  
 For static members located in an external DLL, the section returned by this method may be 0 as this method relies on obtaining the virtual address of the member. Virtual addresses are valid only if the [IDiaSession::put_loadAddress](../debug-interface-access/idiasession--put_loadaddress.md) method in the [IDiaSession](../debug-interface-access/idiasession.md) interface has been called with a nonzero parameter specifying the load address of the DLL.  
  
 To get the offset part of an address, call the [IDiaSymbol::get_addressOffset](../debug-interface-access/idiasymbol--get_addressoffset.md) method.  
  
## Requirements  
  
|Requirement|Description|  
|-----------------|-----------------|  
|Header:|dia2.h|  
|Version:|DIA SDK v7.0|  
  
## See Also  
 [IDiaSymbol](../debug-interface-access/idiasymbol.md)   
 [LocationType Enumeration](../debug-interface-access/locationtype.md)