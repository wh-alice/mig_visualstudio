---
title: "IDebugDocumentTextEvents2::onUpdateTextAttributes | Microsoft Docs"
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
  - "IDebugDocumentTextEvents2::OnUpdateTextAttributes"
helpviewer_keywords: 
  - "IDebugDocumentTextEvents2::onUpdateTextAttributes"
ms.assetid: eb68d69a-1ad9-4ce4-84e1-40979ef16634
caps.latest.revision: 10
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
# IDebugDocumentTextEvents2::onUpdateTextAttributes
Notifies the debug package that text attributes have been updated in the document.  
  
## Syntax  
  
```cpp#  
HRESULT onUpdateTextAttributes(   
   TEXT_POSITION pos,  
   DWORD         dwNumToUpdate  
);  
```  
  
```c#  
int onUpdateTextAttributes(   
   enum_TEXT_POSITION pos,  
   uint               dwNumToUpdate  
);  
```  
  
#### Parameters  
 `pos`  
 [in] A [TEXT_POSITION](../extensibility-debugger-reference/text_position.md) structure that indicates where the text attributes were updated.  
  
 `dwNumToUpdate`  
 [in] Specifies the number of characters of text that were updated.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugDocumentTextEvents2](../extensibility-debugger-reference/idebugdocumenttextevents2.md)   
 [TEXT_POSITION](../extensibility-debugger-reference/text_position.md)