---
title: "Generic type &#39;&lt;generictypename&gt;&#39; cannot be imported more than once | hehe"
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
  - "BC32086"
  - "vbc32086"
helpviewer_keywords: 
  - "BC32086"
ms.assetid: d93bae4b-3224-4a6e-a072-8ce231084519
caps.latest.revision: 9
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
# Generic type &#39;&lt;generictypename&gt;&#39; cannot be imported more than once
An [Imports Statement (.NET Namespace and Type)](../Topic/Imports%20Statement%20\(.NET%20Namespace%20and%20Type\).md) specifies a generic type that has already been imported with different type parameterization.  
  
 You can declare multiple constructed types from a generic type, because you do not redefine the generic type by declaring a constructed type. However, if you import a generic type more than once, that is the equivalent of multiple definitions.  
  
 **Error ID:** BC32086  
  
### To correct this error  
  
1.  If the source file containing this `Imports` statement also contains another `Imports` statement specifying the same generic type, remove one of them.  
  
2.  If you need to import the same generic type with different type parameterizations, use multiple source files.  
  
## See Also  
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)