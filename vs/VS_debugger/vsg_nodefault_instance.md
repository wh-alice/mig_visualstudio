---
title: "VSG_NODEFAULT_INSTANCE"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: na
ms.topic: "article"
ms.assetid: 19c95b0d-9a4d-441f-9ed7-3acb39e67521
caps.latest.revision: 5
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
# VSG_NODEFAULT_INSTANCE
Defines by its presence whether a default instance of the [VsgDbg Class](../VS_debugger/vsgdbg-class.md) class—which provides the programmatic capture interface—is supplied.  
  
## Syntax  
  
```cpp  
#define VSG_NODEFAULT_INSTANCE  
```  
  
## Value  
 A preprocessor symbol that by its presence or absence determines whether a default instance of the `VsgDbg` class is provided. If this symbol is defined, then no default instance of the `VsgDbg` class is provided; otherwise, a default instance is provided and initialized before your program runs.  
  
 The programmatic capture interface is provided through a pointer that has global scope, `g_pVsgDbg`.  
  
```  
VsgDbg *g_pVsgDbg;  
```  
  
## Remarks  
 The default instance is often sufficient, but to use the programmatic capture interface inside a DLL when the D3D device has been created outside that DLL, you must create and manage your own instance of the `VsgDbg` class. If you are managing your own interface to the programmatic capture API in this way, disable the default instance by defining `VSG_NODEFAULT_INSTANCE` to avoid overhead.  
  
 If the default instance is not disabled, it is automatically initialized before your program runs and is automatically destroyed when your program ends. You do not have to initialize or uninitialize this instance explicitly.  
  
 To disable the default instance, you must define `VSG_NODEFAULT_INSTANCE` before you include `vsgcapture.h` in your program.  
  
## Example  
 This example shows how to disable the default instance:  
  
```  
// Define VSG_NODEFAULT_INSTANCE before including vsgcapture.h  
#define VSG_NODEFAULT_INSTANCE  
  
#include <vsgcapture.h>  
```