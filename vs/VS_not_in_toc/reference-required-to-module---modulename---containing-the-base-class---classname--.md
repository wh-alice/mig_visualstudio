---
title: "Reference required to module &#39;&lt;modulename&gt;&#39; containing the base class &#39;&lt;classname&gt;&#39;"
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
  - "vbc30008"
  - "bc30008"
helpviewer_keywords: 
  - "BC30008"
ms.assetid: ec8de475-8a8b-4aa5-86c9-6fcc44dcec06
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
# Reference required to module &#39;&lt;modulename&gt;&#39; containing the base class &#39;&lt;classname&gt;&#39;
Reference required to module '\<modulename>' containing the base class '\<classname>'. Add one to your project.  
  
 The class is defined in a module that is not directly referenced in your project. The [!INCLUDE[vbprvb](../VS_debugger/includes/vbprvb_md.md)] compiler requires a reference to avoid ambiguity in case the class is defined in more than one module.  
  
 **Error ID:** BC30008  
  
### To correct this error  
  
-   Include the name of the unreferenced module in your project references.  
  
## See Also  
 [NIB: Referencing Namespaces and Components](assetId:///568fa759-796b-44cd-bf5e-1cf8de6e38fd)   
 [Troubleshooting Broken References](../VS_IDE/troubleshooting-broken-references.md)