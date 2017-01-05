---
title: "IDebugExpressionEvaluator2"
ms.custom: ""
ms.date: "12/07/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "IDebugExpressionEvaluator2 interface"
ms.assetid: cebe649f-1c77-4d33-854f-30d4f00eceb4
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
# IDebugExpressionEvaluator2
[!INCLUDE[vs2017banner](../../../code-quality/includes/vs2017banner.md)]

> [!IMPORTANT]
>  In Visual Studio 2015, this way of implementing expression evaluators is deprecated. For information about implementing CLR expression evaluators, please see [CLR Expression Evaluators](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) and [Managed Expression Evaluator Sample](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 Represents an enhanced version of an expression evaluator (EE).  
  
## Syntax  
  
```  
IDebugExpressionEvaluator2 : IDebugExpressionEvaluator  
```  
  
## Notes for Implementers  
 This interface is implemented by an expression evaluator.  
  
## Methods  
 In addition to the methods on the [IDebugExpressionEvaluator](../../../extensibility/debugger/reference/idebugexpressionevaluator.md) interface, this interface implements the following methods:  
  
|Method|Description|  
|------------|-----------------|  
|[GetService](../../../extensibility/debugger/reference/idebugexpressionevaluator2--getservice.md)|Retrieves a service object given its unique identifier.|  
|[PreloadModules](../../../extensibility/debugger/reference/idebugexpressionevaluator2--preloadmodules.md)|Preloads the modules designated by the specified symbol provider.|  
|[SetCallback](../../../extensibility/debugger/reference/idebugexpressionevaluator2--setcallback.md)|Enables the expression evaluator (EE) to specify the callback interface the debugger engine (DE) will use to read metric settings.|  
|[SetCorPath](../../../extensibility/debugger/reference/idebugexpressionevaluator2--setcorpath.md)|Sets the path to the common language runtime (CLR) loaded in the debugger.|  
|[SetIDebugIDECallback](../../../extensibility/debugger/reference/idebugexpressionevaluator2--setidebugidecallback.md)|Enables a debug engine to pass a callback to the expression evaluator during initialization.|  
|[Terminate](../../../extensibility/debugger/reference/idebugexpressionevaluator2--terminate.md)|Stops and cleans up the expression evaluator.|  
  
## Requirements  
 Header: Ee.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll