---
title: "IDiaEnumSymbols::get__NewEnum"
ms.custom: na
ms.date: "10/14/2016"
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
  - "IDiaEnumSymbols::get__NewEnum method"
ms.assetid: 879609ea-8e5a-4fa3-afa6-d24870fb4392
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
# IDiaEnumSymbols::get__NewEnum
Retrieves the <xref:System.Runtime.InteropServices.ComTypes.IEnumVARIANT> version of this enumerator.  
  
## Syntax  
  
```cpp#  
HRESULT get__NewEnum (   
   IUnknown** pRetVal  
);  
```  
  
#### Parameters  
 pRetVal  
 [out] Returns the `IUnknown` interface that represents the <xref:System.Runtime.InteropServices.ComTypes.IEnumVARIANT> version of this enumerator.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDiaEnumSymbols](../debugger/idiaenumsymbols.md)