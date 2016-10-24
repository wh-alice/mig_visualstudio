---
title: "IDiaStackWalker::getEnumFrames | testtitle"
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
  - "IDiaStackWalker2::getEnumFrames method"
ms.assetid: f9f09729-4c34-441c-989c-e0b7339ee32c
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
# IDiaStackWalker::getEnumFrames
Retrieves a stack frame enumerator for x86 platforms.  
  
## Syntax  
  
```cpp#  
HRESULT getEnumFrames(   
   IDiaStackWalkHelper*   pHelper,  
   IDiaEnumStackFrames**  ppEnum  
);  
```  
  
#### Parameters  
 `pHelper`  
 [in] The helper [IDiaStackWalkHelper](../debug-interface-access/idiastackwalkhelper.md) object.  
  
 `ppEnum`  
 [out] Returns an [IDiaEnumStackFrames](../debug-interface-access/idiaenumstackframes.md) object that contains a list of [IDiaStackFrame](../debug-interface-access/idiastackframe.md) objects.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 To get a stack frame list on any other platform, call the [IDiaStackWalker::getEnumFrames2](../debug-interface-access/idiastackwalker--getenumframes2.md) method.  
  
## See Also  
 [IDiaStackWalker](../debug-interface-access/idiastackwalker.md)   
 [IDiaStackWalkHelper](../debug-interface-access/idiastackwalkhelper.md)   
 [IDiaStackFrame](../debug-interface-access/idiastackframe.md)   
 [IDiaStackWalker::getEnumFrames2](../debug-interface-access/idiastackwalker--getenumframes2.md)