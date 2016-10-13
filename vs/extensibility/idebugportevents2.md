---
title: "IDebugPortEvents2"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "IDebugPortEvents2"
helpviewer_keywords: 
  - "IDebugPortEvents2 interface"
ms.assetid: 2c017094-3ba2-4067-83f9-147df1d96bce
caps.latest.revision: 18
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
# IDebugPortEvents2
This interface notifies a listener (typically the session debug manager [SDM] or a debug engine) of process and program creation and destruction on a particular port. This information can be used to present a real-time view of the processes and programs running on the port.  
  
## Syntax  
  
```  
IDebugPortEvents2 : IUnknown  
```  
  
## Notes for Implementers  
 Visual Studio typically implements this interface to receive notifications about program creation and destruction. A debug engine can also implement this interface to listen for such port events.  
  
## Notes for Callers  
 All [IDebugPort2](../extensibility/idebugport2.md) interfaces can be queried for an \<xref:System.Runtime.InteropServices.ComTypes.IConnectionPointContainer> interface. Then the \<xref:System.Runtime.InteropServices.ComTypes.IConnectionPointContainer.FindConnectionPoint*> method for `IDebugPortEvents2` is called in the \<xref:System.Runtime.InteropServices.ComTypes.IConnectionPointContainer> interface to get an \<xref:System.Runtime.InteropServices.ComTypes.IConnectionPoint> interface. Finally, the \<xref:System.Runtime.InteropServices.ComTypes.IConnectionPoint.Advise*> method in the \<xref:System.Runtime.InteropServices.ComTypes.IConnectionPoint> interface is called to send the events through the [Event](../extensibility/idebugportevents2--event.md) method.  
  
## Methods in Vtable Order  
 The following table shows the method of `IDebugPortEvents2`.  
  
|Method|Description|  
|------------|-----------------|  
|[Event](../extensibility/idebugportevents2--event.md)|Sends events that describe the creation and destruction of processes and programs on the port.|  
  
## Remarks  
 `IDebugPortEvents2` is also used by the SDM to debug programs that run in a process that is already being debugged.  
  
 Port events are passed to the SDM by this interface.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../extensibility/core-interfaces.md)   
 [IDebugPort2](../extensibility/idebugport2.md)