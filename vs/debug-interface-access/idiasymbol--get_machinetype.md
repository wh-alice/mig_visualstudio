---
title: "IDiaSymbol::get_machineType | testtitle"
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
  - "IDiaSymbol::get_machineType method"
ms.assetid: 30870b10-6f32-45c6-a0d7-020dea707710
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
# IDiaSymbol::get_machineType
Retrieves the type of the target CPU.  
  
## Syntax  
  
```cpp#  
HRESULT get_machineType (   
   DWORD* pRetVal  
);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] Returns a value from the [CV_CPU_TYPE_e Enumeration](../debug-interface-access/cv_cpu_type_e.md) enumeration that specifies the target CPU type.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE` or an error code.  
  
> [!NOTE]
>  A return value of `S_FALSE` means the property is not available for the symbol.  
  
## See Also  
 [CV_CPU_TYPE_e Enumeration](../debug-interface-access/cv_cpu_type_e.md)   
 [IDiaSymbol](../debug-interface-access/idiasymbol.md)