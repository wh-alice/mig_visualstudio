---
title: "&#39;&lt;method1&gt;&#39; cannot override &#39;&lt;method2&gt;&#39; because they differ by optional parameters"
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
  - "vbc30308"
  - "bc30308"
helpviewer_keywords: 
  - "BC30308"
ms.assetid: 591dc351-4b87-4e92-81e1-2c1ff51da295
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
# &#39;&lt;method1&gt;&#39; cannot override &#39;&lt;method2&gt;&#39; because they differ by optional parameters
You have attempted to override a method with another method that differs from the first in the values of its optional parameters, meaning that their signatures differ. A type may override an inherited overridable method by declaring a method with the same name and signature, and marking the declaration with the `Overrides` modifier.  
  
 **Error ID:** BC30308  
  
### To correct this error  
  
-   Make sure the two methods have the same signature.  
  
## See Also  
 [NOT IN BUILD: Overriding Properties and Methods](http://msdn.microsoft.com/2167e8f5-1225-4b13-9ebd-02591ba90213)   
 [Overrides](../Topic/Overrides%20\(Visual%20Basic\).md)