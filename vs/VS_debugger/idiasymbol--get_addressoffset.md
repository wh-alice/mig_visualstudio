---
title: "IDiaSymbol::get_addressOffset"
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
  - "IDiaSymbol::get_addressOffset method"
ms.assetid: c15639b0-7f37-46c7-891b-40273b7f6319
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
# IDiaSymbol::get_addressOffset
Retrieves the offset part of an address location. Use when the [LocationType Enumeration](../VS_debugger/locationtype.md) is set to `LocIsStatic`.  
  
## Syntax  
  
```cpp#  
HRESULT get_addressOffset (   
   DWORD* pRetVal  
);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] Returns the offset part of an address location.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE` or an error code.  
  
> [!NOTE]
>  A return value of `S_FALSE` means that the property is not available for the symbol.  
  
## Remarks  
 For static members located in an external DLL, the offset returned by this method may be 0 as this method relies on obtaining the virtual address of the member. Virtual addresses are valid only if the [IDiaSession::put_loadAddress](../VS_debugger/idiasession--put_loadaddress.md) method in the [IDiaSession](../VS_debugger/idiasession.md) interface has been called with a nonzero parameter specifying the load address of the DLL.  
  
 To get the section part of an address, call the [IDiaSymbol::get_addressSection](../VS_debugger/idiasymbol--get_addresssection.md) method.  
  
## Requirements  
  
|Requirement|Description|  
|-----------------|-----------------|  
|Header:|dia2.h|  
|Version:|DIA SDK v7.0|  
  
## See Also  
 [IDiaSymbol](../VS_debugger/idiasymbol.md)   
 [LocationType Enumeration](../VS_debugger/locationtype.md)   
 [IDiaSymbol::get_addressSection](../VS_debugger/idiasymbol--get_addresssection.md)   
 [IDiaSession::put_loadAddress](../VS_debugger/idiasession--put_loadaddress.md)   
 [IDiaSession](../VS_debugger/idiasession.md)