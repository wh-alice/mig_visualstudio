---
title: "Reference required to module &#39;&lt;modulename&gt;&#39; containing the type &#39;&lt;membername&gt;&#39; | testtitle"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "bc30653"
  - "vbc30653"
helpviewer_keywords: 
  - "BC30653"
ms.assetid: dad8a808-d7d3-4c80-91b1-458070dec63d
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
# Reference required to module &#39;&lt;modulename&gt;&#39; containing the type &#39;&lt;membername&gt;&#39;
Reference required to module '\<modulename>' containing the type '\<membername>'. Add one to your project.  
  
 The project contains a type that depends on another type from an assembly that is not included in the project references.  
  
 **Error ID:** BC30653  
  
### To correct this error  
  
-   Add a project reference for the dependent types in the project.  
  
## See Also  
 [Managing references in a project](../ide/managing-references-in-a-project.md)