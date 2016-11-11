---
title: "&lt;specifier1&gt; &lt;type&gt; cannot inherit from a &lt;specifier2&gt; &lt;type&gt; because it expands the access of the base &lt;type&gt; | Microsoft Docs"
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
  - "bc30509"
  - "vbc30509"
helpviewer_keywords: 
  - "BC30509"
ms.assetid: 53594d6e-5e6d-463d-aa68-e2d41e152da7
caps.latest.revision: 8
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
# &lt;specifier1&gt; &lt;type&gt; cannot inherit from a &lt;specifier2&gt; &lt;type&gt; because it expands the access of the base &lt;type&gt;
You have attempted to have a public class inherit from a base class marked `Private` or `Friend`.  
  
 **Error ID:** BC30509  
  
### To correct this error  
  
-   Declare the base class `Public` or declare the inheriting class `Private` or `Friend`.  
  
## See Also  
 [NOT IN BUILD: Inheritance in Visual Basic](http://msdn.microsoft.com/en-us/e5e6e240-ed31-4657-820c-079b7c79313c)