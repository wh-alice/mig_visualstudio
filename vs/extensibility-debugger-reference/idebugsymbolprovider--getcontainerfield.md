---
title: "IDebugSymbolProvider::GetContainerField | hehe"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "IDebugSymbolProvider::GetContainerField"
helpviewer_keywords: 
  - "IDebugSymbolProvider::GetContainerField method"
ms.assetid: d6b56b4f-a96b-4fa7-87c1-bac4e58fa766
caps.latest.revision: 11
ms.author: "gregvanl"
manager: "ghogen"
translation.priority.mt: 
  - "cs-cz"
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "pl-pl"
  - "pt-br"
  - "ru-ru"
  - "tr-tr"
  - "zh-cn"
  - "zh-tw"
---
# IDebugSymbolProvider::GetContainerField
This method gets the field that contains the debug address.  
  
## Syntax  
  
```cpp#  
HRESULT GetContainerField(   
   IDebugAddress*         pAddress,  
   IDebugContainerField** ppContainerField  
);  
```  
  
```c#  
int GetContainerField(  
   IDebugAddress            pAddress,   
   out IDebugContainerField ppContainerField  
);  
```  
  
#### Parameters  
 `pAddress`  
 [in] The address as represented by an [IDebugAddress](../extensibility-debugger-reference/idebugaddress.md) interface.  
  
 `ppContainerField`  
 [out] Returns a container field represented by an [IDebugContainerField](../extensibility-debugger-reference/idebugcontainerfield.md) interface.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugSymbolProvider](../extensibility-debugger-reference/idebugsymbolprovider.md)   
 [IDebugAddress](../extensibility-debugger-reference/idebugaddress.md)   
 [IDebugContainerField](../extensibility-debugger-reference/idebugcontainerfield.md)