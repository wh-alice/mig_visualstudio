---
title: "Generic methods cannot be exposed to COM"
ms.custom: na
ms.date: "10/01/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "vbc30943"
  - "bc30943"
helpviewer_keywords: 
  - "BC30943"
ms.assetid: 0e3bff62-f187-4864-8520-70f6be22e869
caps.latest.revision: 8
ms.author: "billchi"
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
# Generic methods cannot be exposed to COM
A [!INCLUDE[dnprdnshort](../VS_debugger/includes/dnprdnshort_md.md)] component containing one or more generic procedures is exported to a COM component.  
  
 The Component Object Model (COM) does not support generic types, and it cannot interoperate with them.  
  
 **Error ID:** BC30943  
  
### To correct this error  
  
-   Remove the generic procedure or procedures from the [!INCLUDE[dnprdnshort](../VS_debugger/includes/dnprdnshort_md.md)] component, or do not use it for COM interop.  
  
## See Also  
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [COM Interop](../Topic/COM%20Interop%20\(Visual%20Basic\).md)