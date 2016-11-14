---
title: "Troubleshooting Exceptions: System.Runtime.InteropServices.COMException | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "EHCOM"
dev_langs: 
  - "JScript"
  - "VB"
  - "CSharp"
  - "C++"
helpviewer_keywords: 
  - "COMException class"
ms.assetid: 14b6de51-e039-4db7-9321-06c9e16e328a
caps.latest.revision: 14
author: "mikeblome"
ms.author: "mblome"
manager: "douge"
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
# Troubleshooting Exceptions: System.Runtime.InteropServices.COMException
A <xref:System.Runtime.InteropServices.COMException> exception is thrown when an unrecognized HRESULT is returned from a COM method call.  
  
## Associated Tips  
 **Check the ErrorCode property of the exception to determine the HRESULT returned by the COM object**  
 When the runtime encounters an unfamiliar HRESULT, it throws a <xref:System.Runtime.InteropServices.COMException> exception, which includes a public `ErrorCode` property that contains the HRESULT returned by the call. If an error message is available to the runtime, the message is returned to the caller. However, if the COM component developer fails to include an error message, the runtime returns the eight-digit HRESULT in place of a message string. Having an HRESULT allows the caller to determine the cause of the exception. For more information, see [How to: Map HRESULTs and Exceptions](http://msdn.microsoft.com/en-us/Library/610b364b-2761-429d-9c4a-afbc3e66f1b9).  
  
 **Disable the hosting process.**  
 COM is used to communicate between [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] and the hosting process. Because it is used before code runs, a call to `CoInitializeSecurity` causes this exception to be thrown.  
  
### Remarks  
 The common language runtime (CLR) transforms well-known HRESULTS to .NET exceptions, enabling COM objects to return meaningful error information to managed clients. The HRESULT to exception mapping also works in the other direction by returning specific HRESULTS to unmanaged clients.  
  
 When passing late-bound parameters to methods of Microsoft Office objects, a <xref:System.Runtime.InteropServices.COMException> exception may be thrown when the objects are COM objects. The late binder assumes that such method calls involve a `ByRef` parameter and that the property you pass has a `Set` accessor. If the property does not, the [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] generates a <xref:System.MissingMethodException> exception (HRESULT CORE_E_MISSINGMETHOD). To work around this behavior, use early-bound objects or pass a variable instead of a property of the object.  
  
## See Also  
 <xref:System.Runtime.InteropServices.COMException>   
 [Use the Exception Assistant](http://msdn.microsoft.com/en-us/Library/e0a78c50-7318-4d54-af51-40c00aea8711)   
 [Handling COM Interop Exceptions](http://msdn.microsoft.com/en-us/Library/e6104aa8-8e5f-4069-b864-def85579c96c)