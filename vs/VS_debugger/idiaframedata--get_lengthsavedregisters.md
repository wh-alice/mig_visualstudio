---
title: "IDiaFrameData::get_lengthSavedRegisters"
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
  - "IDiaFrameData::get_lengthSavedRegisters method"
ms.assetid: dfda4e91-9bfa-4b9d-9133-b73015bfa4d5
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
# IDiaFrameData::get_lengthSavedRegisters
Retrieves the number of bytes of saved registers pushed on the stack.  
  
## Syntax  
  
```cpp#  
HRESULT get_lengthSavedRegisters (   
   DWORD* pRetVal  
);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] Returns the number of bytes of saved registers.  
  
## Return Value  
 If successful, returns `S_OK`. Returns `S_FALSE` if this property is not supported. Otherwise, returns an error code.  
  
## Remarks  
 The value returned by this method is typically used in the interpretation of a program string (see the [IDiaFrameData::get_program](../VS_debugger/idiaframedata--get_program.md) method for the definition of a program string).  
  
## See Also  
 [IDiaFrameData](../VS_debugger/idiaframedata.md)   
 [IDiaFrameData::get_program](../VS_debugger/idiaframedata--get_program.md)