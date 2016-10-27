---
title: "Stepping in Break Mode"
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
  - "break mode, stepping"
  - "stepping, in break mode"
  - "debugging [Debugging SDK], stepping in break mode"
ms.assetid: b08dc8ee-6c63-4462-a097-6f525cfbb35a
caps.latest.revision: 7
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
# Stepping in Break Mode
The following describes the process that occurs when the debugger is in break mode and must step through code:  
  
## Stepping Process  
  
1.  Call [IDebugProgram2::Step](../../extensibility/debugger/reference/idebugprogram2--step.md) with [STEPKIND](../../extensibility/debugger/reference/stepkind.md) and [STEPUNIT](../../extensibility/debugger/reference/stepunit.md) arguments to execute a step.  
  
2.  When the step is finished, send an [IDebugStepCompleteEvent2](../../extensibility/debugger/reference/idebugstepcompleteevent2.md) as a stopping event.  
  
## See Also  
 [Calling Debugger Events](../../extensibility/debugger/calling-debugger-events.md)