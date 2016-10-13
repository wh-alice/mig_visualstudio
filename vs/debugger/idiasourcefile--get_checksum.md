---
title: "IDiaSourceFile::get_checksum"
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
  - "IDiaSourceFile::get_checksum method"
ms.assetid: aad63a7e-4e22-44e4-8a5b-81b5174ced1e
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
# IDiaSourceFile::get_checksum
Retrieves the checksum bytes.  
  
## Syntax  
  
```cpp#  
HRESULT get_checksum (   
   DWORD  cbData,  
   DWORD* pcbData,  
   BYTE   data[]  
);  
```  
  
#### Parameters  
 `cbData`  
 [in] Size of the data buffer, in bytes.  
  
 `pcbData`  
 [out] Returns the number of checksum bytes. This parameter cannot be `NULL`.  
  
 `data`  
 [in, out] A buffer that is filled with the checksum bytes. If this parameter is `NULL`, then `pcbData` returns the number of bytes required.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 To determine the type of checksum algorithm that was used to generate the checksum bytes, call the [IDiaSourceFile::get_checksumType](../debugger/idiasourcefile--get_checksumtype.md) method.  
  
 The checksum is typically generated from the image of the source file so changes in the source file are reflected in changes in the checksum bytes. If the checksum bytes do not match a checksum generated from the loaded image of the file, then the file should be considered damaged or tampered with.  
  
 Typical checksums are never more than 32 bytes in size but do not assume that is the maximum size of a checksum. Set the `data` parameter to `NULL` to get the number of bytes required to retrieve the checksum. Then allocate a buffer of the appropriate size and call this method once more with the new buffer.  
  
## See Also  
 [IDiaSourceFile](../debugger/idiasourcefile.md)   
 [IDiaSourceFile::get_checksumType](../debugger/idiasourcefile--get_checksumtype.md)