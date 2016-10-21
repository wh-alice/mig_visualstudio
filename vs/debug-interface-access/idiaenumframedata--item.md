---
title: "IDiaEnumFrameData::Item | hehe"
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
  - "IDiaEnumFrameData::Item method"
ms.assetid: 2761a72d-1868-4f5b-a32e-c2a1d9358c91
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
# IDiaEnumFrameData::Item
Retrieves a frame data element by means of an index.  
  
## Syntax  
  
```cpp#  
HRESULT Item (   
   DWORD           index,  
   IDiaFrameData** section  
);  
```  
  
#### Parameters  
 index  
 [in] Index of the [IDiaFrameData](../debug-interface-access/idiaframedata.md) object to be retrieved. The index is in the range 0 to `count`-1, where `count` is returned by the [IDiaEnumFrameData::get_Count](../debug-interface-access/idiaenumframedata--get_count.md) method.  
  
 section  
 [out] Returns an [IDiaFrameData](../debug-interface-access/idiaframedata.md) object representing the desired frame data element.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDiaEnumFrameData](../debug-interface-access/idiaenumframedata.md)   
 [IDiaFrameData](../debug-interface-access/idiaframedata.md)