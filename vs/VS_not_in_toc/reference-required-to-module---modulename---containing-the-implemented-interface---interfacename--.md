---
title: "Reference required to module &#39;&lt;modulename&gt;&#39; containing the implemented interface &#39;&lt;interfacename&gt;&#39;"
ms.custom: na
ms.date: "10/10/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "vbc30010"
  - "bc30010"
helpviewer_keywords: 
  - "BC30010"
ms.assetid: 57fe7e15-bf99-49d1-ba6c-bb7abeb615b1
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
# Reference required to module &#39;&lt;modulename&gt;&#39; containing the implemented interface &#39;&lt;interfacename&gt;&#39;
Reference required to module '\<modulename>' containing the implemented interface '\<interfacename>'. Add one to your project.  
  
 The interface is defined in a module that is not directly referenced in your project. The [!INCLUDE[vbprvb](../VS_debugger/includes/vbprvb_md.md)] compiler requires a reference to avoid ambiguity in case the interface is defined in more than one module.  
  
 **Error ID:** BC30010  
  
### To correct this error  
  
-   Include the name of the unreferenced module in your project references.  
  
## See Also  
 [NIB: Referencing Namespaces and Components](assetId:///568fa759-796b-44cd-bf5e-1cf8de6e38fd)   
 [Troubleshooting Broken References](../VS_IDE/troubleshooting-broken-references.md)