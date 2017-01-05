---
title: "How to: Get a Service from the DTE Object"
ms.custom: ""
ms.date: "12/05/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "services, from the DTE object"
ms.assetid: c26a51d4-86f0-454b-9625-5443e55eec7d
caps.latest.revision: 13
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
# How to: Get a Service from the DTE Object
A service can be obtained from any program that has access to the [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] Automation <xref:EnvDTE.DTEClass> object. For example, you can access the <xref:Microsoft.VisualStudio.Shell.Interop.SVsActivityLog> service from a wizard through the DTE object. You can use this service to write to the activity log. For more information, see [How to: Use the Activity Log](../extensibility/how-to--use-the-activity-log.md).  
  
 The DTE object implements <xref:Microsoft.VisualStudio.OLE.Interop.IServiceProvider>, which you can use to query for a service from managed code by using <xref:Microsoft.VisualStudio.Shell.ServiceProvider.GetService%2A>.  
  
### To get a service from the DTE object  
  
1.  The following code creates a <xref:Microsoft.VisualStudio.Shell.ServiceProvider> from the DTE object and calls <xref:Microsoft.VisualStudio.Shell.ServiceProvider.GetService%2A> with the type of the <xref:Microsoft.VisualStudio.Shell.Interop.SVsActivityLog> service. The service is cast to the interface <xref:Microsoft.VisualStudio.Shell.Interop.IVsActivityLog>, which is used to write an entry in the activity log. For more information abou how to write to the activity log, see [How to: Use the Activity Log](../extensibility/how-to--use-the-activity-log.md).  
  
     [!code-cs[GetAServiceFromTheDTEObject#1](../misc/codesnippet/CSharp/how-to--get-a-service-from-the-dte-object_1.cs)]
     [!code-vb[GetAServiceFromTheDTEObject#1](../misc/codesnippet/VisualBasic/how-to--get-a-service-from-the-dte-object_1.vb)]  
  
## See Also  
 [Using and Providing Services](../extensibility/using-and-providing-services.md)   
 [Service Essentials](../extensibility/internals/service-essentials.md)