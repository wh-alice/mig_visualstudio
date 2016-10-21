---
title: "Structures cannot declare a non-shared &#39;Sub New&#39; with no parameters | hehe"
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
  - "vbc30629"
  - "bc30629"
helpviewer_keywords: 
  - "BC30629"
ms.assetid: f4298ef7-85b1-4543-b764-4c3abda84baa
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
# Structures cannot declare a non-shared &#39;Sub New&#39; with no parameters
`Sub New` constructors declared within structures must either accept arguments or be declared with the `Shared` modifier.  
  
 **Error ID:** BC30629  
  
### To correct this error  
  
-   Change the `Sub New` constructor so that it accepts arguments.  
  
-   Apply the `Shared` modifier to make the constructor shared.  
  
## See Also  
 [Structure Statement](../Topic/Structure%20Statement.md)   
 [Structures](../Topic/Structures%20\(Visual%20Basic\).md)