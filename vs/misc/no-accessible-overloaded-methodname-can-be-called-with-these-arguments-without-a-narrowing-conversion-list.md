---
title: "No accessible overloaded &#39;&lt;methodname&gt;&#39; can be called with these arguments without a narrowing conversion: &lt;list&gt; | Microsoft Docs"
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
  - "vbrAmbiguousCall2"
ms.assetid: 13b20ffa-9f02-4971-a3cb-e08b402fd971
caps.latest.revision: 9
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
# No accessible overloaded &#39;&lt;methodname&gt;&#39; can be called with these arguments without a narrowing conversion: &lt;list&gt;
An overloaded method was called, but the method cannot be matched with the list of provided arguments without a narrowing conversion.  
  
### To correct this error  
  
1.  Specify `Option``Strict` `Off`.  
  
2.  Change the arguments to match a signature of the overloaded method.  
  
## See Also  
 [Passing Arguments by Value and by Reference](/dotnet/visual-basic/language-reference/procedures/passing-arguments-by-value-and-by-reference)   
 [Widening and Narrowing Conversions](/dotnet/visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions)