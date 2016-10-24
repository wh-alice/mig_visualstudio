---
title: "IDiaStackWalkHelper::frameForVA | Microsoft Docs"
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
  - "IDiaStackWalkHelper2::frameForVA method"
ms.assetid: f35fc61b-f8dd-473a-b583-82c304059422
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
# IDiaStackWalkHelper::frameForVA
Retrieves the stack frame that contains the specified virtual address.  
  
## Syntax  
  
```cpp#  
HRESULT frameForVA(   
   ULONGLONG        va,  
   IDiaFrameData**  ppFrame  
);  
```  
  
#### Parameters  
 `va`  
 [in] The virtual address for the frame data.  
  
 `ppFrame`  
 [out] An [IDiaFrameData](../debug-interface-access/idiaframedata.md) object that represents the stack frame at the specified address.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDiaStackWalkHelper](../debug-interface-access/idiastackwalkhelper.md)   
 [IDiaFrameData](../debug-interface-access/idiaframedata.md)