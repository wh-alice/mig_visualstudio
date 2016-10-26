---
title: "Reference required to assembly &#39;&lt;assemblyname&gt;&#39; containing the implemented interface &#39;&lt;interfacename&gt;&#39;"
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
  - "vbc30009"
  - "bc30009"
helpviewer_keywords: 
  - "BC30009"
ms.assetid: b2dfb89d-7fde-4a8e-ba7f-fe1e59eabaca
caps.latest.revision: 8
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
# Reference required to assembly &#39;&lt;assemblyname&gt;&#39; containing the implemented interface &#39;&lt;interfacename&gt;&#39;
Reference required to assembly '\<assemblyname>' containing the implemented interface '\<interfacename>'. Add one to your project.  
  
 The interface is defined in a dynamic-link library (DLL) or assembly that is not directly referenced in your project. The [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] compiler requires a reference to avoid ambiguity in case the interface is defined in more than one DLL or assembly.  
  
 **Error ID:** BC30009  
  
### To correct this error  
  
-   Include the name of the unreferenced DLL or assembly in your project references.  
  
## See Also  
 [NIB: Referencing Namespaces and Components](http://msdn.microsoft.com/en-us/568fa759-796b-44cd-bf5e-1cf8de6e38fd)   
 [Troubleshooting Broken References](../ide/troubleshooting-broken-references.md)