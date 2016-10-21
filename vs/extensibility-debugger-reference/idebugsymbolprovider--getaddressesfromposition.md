---
title: "IDebugSymbolProvider::GetAddressesFromPosition | hehe"
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
  - "IDebugSymbolProvider::GetAddressesFromPosition"
helpviewer_keywords: 
  - "IDebugSymbolProvider::GetAddressesFromPosition method"
ms.assetid: 1b0f02cb-8ace-4614-88f3-0e10239012b3
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
# IDebugSymbolProvider::GetAddressesFromPosition
This method maps a document position into an array of debug addresses.  
  
## Syntax  
  
```cpp#  
HRESULT GetAddressesFromPosition(   
   IDebugDocumentPosition2* pDocPos,  
   BOOL                     fStatmentOnly,  
   IEnumDebugAddresses**    ppEnumBegAddresses,  
   IEnumDebugAddresses**    ppEnumEndAddresses  
);  
```  
  
```c#  
int GetAddressesFromPosition(   
   IDebugDocumentPosition2  pDocPos,  
   bool                     fStatmentOnly,  
   out IEnumDebugAddresses  ppEnumBegAddresses,  
   out IEnumDebugAddresses  ppEnumEndAddresses  
);  
```  
  
#### Parameters  
 `pDocPos`  
 [in] The document position.  
  
 `fStatmentOnly`  
 [in] If TRUE, limits the debug addresses to a single statement.  
  
 `ppEnumBegAddresses`  
 [out] Returns an enumerator for the starting debug addresses associated with this statement or line.  
  
 `ppEnumEndAddresses`  
 [out] Returns an [IEnumDebugAddresses](../extensibility-debugger-reference/ienumdebugaddresses.md) enumerator for the ending debug addresses associated with this statement or line.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 A document position typically indicates a range of source lines. This method provides the starting and ending debug addresses associated with these lines. Some languages allow statements that span multiple lines, or lines that contains more than one statement. This method provides a flag to limit the debug addresses to a single statement.  
  
 It is possible for a single statement to have multiple debug addresses, as in the case of templates.  
  
## See Also  
 [IDebugSymbolProvider](../extensibility-debugger-reference/idebugsymbolprovider.md)   
 [GetAddressesFromContext](../extensibility-debugger-reference/idebugsymbolprovider--getaddressesfromcontext.md)   
 [IEnumDebugAddresses](../extensibility-debugger-reference/ienumdebugaddresses.md)