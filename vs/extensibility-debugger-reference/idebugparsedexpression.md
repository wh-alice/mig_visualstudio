---
title: "IDebugParsedExpression | hehe"
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
  - "IDebugParsedExpression"
helpviewer_keywords: 
  - "IDebugParsedExpression interface"
ms.assetid: be6486ed-b070-4898-95b1-58581bcb4447
caps.latest.revision: 12
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
# IDebugParsedExpression
> [!IMPORTANT]
>  In Visual Studio 2015, this way of implementing expression evaluators is deprecated. For information about implementing CLR expression evaluators, please see [CLR Expression Evaluators](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) and [Managed Expression Evaluator Sample](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 This interface represents a parsed expression ready to be evaluated.  
  
## Syntax  
  
```  
IDebugParsedExpression : IUnknown  
```  
  
## Notes for Implementers  
 An expression evaluator implements this interface to represent a parsed expression that is ready for evaluation.  
  
## Notes for Callers  
 A call to [Parse](../extensibility-debugger-reference/idebugexpressionevaluator--parse.md) returns this interface.  
  
## Methods in Vtable Order  
 The following table shows the method of `IDebugParsedExpression`.  
  
|Method|Description|  
|------------|-----------------|  
|[EvaluateSync](../extensibility-debugger-reference/idebugparsedexpression--evaluatesync.md)|Evaluates the parsed expression.|  
  
## Remarks  
 When the caller is ready to evaluate the expression, it calls [EvaluateSync](../extensibility-debugger-reference/idebugparsedexpression--evaluatesync.md) to return an [IDebugProperty2](../extensibility-debugger-reference/idebugproperty2.md) that contains the result of the evaluation. This two-part approach to evaluation, parsing then evaluating, enables the parsed expression to be evaluated multiple times, bypassing the time-consuming process of parsing the expression.  
  
## Requirements  
 Header: ee.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Parse](../extensibility-debugger-reference/idebugexpressionevaluator--parse.md)   
 [EvaluateSync](../extensibility-debugger-reference/idebugparsedexpression--evaluatesync.md)   
 [IDebugProperty2](../extensibility-debugger-reference/idebugproperty2.md)