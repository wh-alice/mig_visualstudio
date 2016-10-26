---
title: "IDiaAddressMap"
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
  - "IDiaAddressMap interface"
ms.assetid: e6467529-508c-4328-85d7-89444ae4d1c1
caps.latest.revision: 10
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
# IDiaAddressMap
Provides control over how the DIA SDK computes virtual and relative virtual addresses for debug objects.  
  
## Syntax  
  
```  
IDiaAddressMap : IUnknown  
```  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDiaAddressMap`.  
  
|Method|Description|  
|------------|-----------------|  
|[IDiaAddressMap::get_addressMapEnabled](../debug-interface-access/idiaaddressmap--get_addressmapenabled.md)|Indicates whether an address map has been established for a particular session.|  
|[IDiaAddressMap::put_addressMapEnabled](../debug-interface-access/idiaaddressmap--put_addressmapenabled.md)|Specifies whether the address map should be used to translate symbol addresses.|  
|[IDiaAddressMap::get_relativeVirtualAddressEnabled](../debug-interface-access/idiaaddressmap--get_relativevirtualaddressenabled.md)|Indicates whether the calculation and use of relative virtual addresses is enabled.|  
|[IDiaAddressMap::put_relativeVirtualAddressEnabled](../debug-interface-access/idiaaddressmap--put_relativevirtualaddressenabled.md)|Allows the client to enable or disable the calculation of relative virtual addresses.|  
|[IDiaAddressMap::get_imageAlign](../debug-interface-access/idiaaddressmap--get_imagealign.md)|Retrieves the current image alignment.|  
|[IDiaAddressMap::put_imageAlign](../debug-interface-access/idiaaddressmap--put_imagealign.md)|Sets the image alignment.|  
|[IDiaAddressMap::set_imageHeaders](../debug-interface-access/idiaaddressmap--set_imageheaders.md)|Sets image headers to enable the translation of relative virtual addresses.|  
|[IDiaAddressMap::set_addressMap](../debug-interface-access/idiaaddressmap--set_addressmap.md)|Provides an address map to support image layout translations.|  
  
## Remarks  
 The control provided by this interface is encapsulated in two sets of data you supply: image headers and address maps. Most clients use the [IDiaDataSource::loadDataForExe](../debug-interface-access/idiadatasource--loaddataforexe.md) method to find the proper debug information for an image and the method can typically discover all of the necessary headers and maps data itself. However some clients implement specialized processing and searching for data. Such clients use the methods of the `IDiaAddressMap` interface to provide the DIA SDK with the search results.  
  
## Notes for Callers  
 This interface is available from the DIA session object. The client calls the `QueryInterface` method on DIA session object interface, usually [IDiaSession](../debug-interface-access/idiasession.md), to retrieve the `IDiaAddressMap` interface.  
  
## Requirements  
 Header: Dia2.h  
  
 Library: diaguids.lib  
  
 DLL: msdia80.dll  
  
## See Also  
 [Interfaces (Debug Interface Access SDK)](../debug-interface-access/interfaces--debug-interface-access-sdk-.md)   
 [IDiaDataSource::loadDataForExe](../debug-interface-access/idiadatasource--loaddataforexe.md)   
 [IDiaSession](../debug-interface-access/idiasession.md)