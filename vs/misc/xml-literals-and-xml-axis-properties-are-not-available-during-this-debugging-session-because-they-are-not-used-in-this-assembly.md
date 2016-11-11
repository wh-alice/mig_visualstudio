---
title: "XML literals and XML axis properties are not available during this debugging session because they are not used in this assembly | Microsoft Docs"
ms.custom: ""
ms.date: "2015-07-20"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc31196"
  - "bc31196"
helpviewer_keywords: 
  - "BC31196"
ms.assetid: 36be5c92-dd6b-41d4-894a-2bd71d772092
caps.latest.revision: 6
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
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
# XML literals and XML axis properties are not available during this debugging session because they are not used in this assembly
An XML literal or XML axis property has been referenced in the **Watch** or **Immediate** window during a debugging session in which XML in [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] features are not available. This is the case for an assembly that either does not use the XML in [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] features or is a release build.  
  
 **Error ID:** BC31196  
  
### To correct this error  
  
-   Start a new debugging session using the debug build of the assembly.  
  
## See Also  
 [Debugging Your Visual Basic Application](/dotnet/visual-basic/developing-apps/debugging)   
 [XML Literals](/dotnet/visual-basic/language-reference/xml-literals/index)   
 [XML Axis Properties](/dotnet/visual-basic/language-reference/xml-axis/xml-axis-properties)   
 [XML](/dotnet/visual-basic/programming-guide/language-features/xml/index)