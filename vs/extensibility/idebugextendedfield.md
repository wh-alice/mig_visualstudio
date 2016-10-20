---
title: "IDebugExtendedField | Microsoft Docs"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "IDebugExtendedField interface"
ms.assetid: b491499c-af57-47da-87d6-34b7398f6591
caps.latest.revision: 6
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
# IDebugExtendedField
Extends the types of fields that are available to support managed code generics.  
  
## Syntax  
  
```  
IDebugExtendedField : IDebugField  
```  
  
## Methods  
 In addition to the methods on the [IDebugField](../extensibility/idebugfield.md) interface, this interface implements the following methods:  
  
|Method|Description|  
|------------|-----------------|  
|[GetExtendedKind](../extensibility/idebugextendedfield--getextendedkind.md)|Retrieves the specified extended field kind.|  
|[IsClosedType](../extensibility/idebugextendedfield--isclosedtype.md)|Determines if the field represents a closed type.|  
  
## Requirements  
 Header: Sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll