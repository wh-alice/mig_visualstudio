---
title: "IDiaAddressMap::get_addressMapEnabled | hehe"
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
  - "IDiaAddressMap::get_addressMapEnabled method"
ms.assetid: 6183dc5e-befa-4e5a-ae5a-f4aa24f3ed9e
caps.latest.revision: 7
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
# IDiaAddressMap::get_addressMapEnabled
Indicates whether an address map has been established for a particular session.  
  
## Syntax  
  
```cpp#  
HRESULT get_addressMapEnabled (   
   BOOL* pRetVal  
);  
```  
  
#### Parameters  
 pRetVal  
 [out] Returns `TRUE` if the address mapping is enabled.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 Executable post-processors sometimes update the executable. DIA contains a mechanism to support the translation of symbols to the new layout.  
  
 Client applications can set the address map for a particular session by getting the [IDiaAddressMap](../debug-interface-access/idiaaddressmap.md) interface from the [IDiaSession](../debug-interface-access/idiasession.md) interface and calling the [IDiaAddressMap::set_addressMap](../debug-interface-access/idiaaddressmap--set_addressmap.md) method followed by a call to the [IDiaAddressMap::put_addressMapEnabled](../debug-interface-access/idiaaddressmap--put_addressmapenabled.md) method. The `get_addressMapEnabled` method returns the results of calling the `put_addressMapEnabled` method.  
  
## See Also  
 [IDiaAddressMap](../debug-interface-access/idiaaddressmap.md)   
 [IDiaSession](../debug-interface-access/idiasession.md)   
 [IDiaAddressMap::set_addressMap](../debug-interface-access/idiaaddressmap--set_addressmap.md)   
 [IDiaAddressMap::put_addressMapEnabled](../debug-interface-access/idiaaddressmap--put_addressmapenabled.md)