---
title: "&#39;&lt;classname1&gt;&#39; cannot inherit from &lt;type&gt; &#39;&lt;classname2&gt;&#39; because &#39;&lt;classname2&gt;&#39; is declared &#39;NotInheritable&#39; | Microsoft Docs"
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
  - "vbc30299"
  - "bc30299"
helpviewer_keywords: 
  - "BC30299"
ms.assetid: 627d50f5-9e75-495d-93f7-50096ba2ea08
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
# &#39;&lt;classname1&gt;&#39; cannot inherit from &lt;type&gt; &#39;&lt;classname2&gt;&#39; because &#39;&lt;classname2&gt;&#39; is declared &#39;NotInheritable&#39;
A class attempts to inherit from another class, but the desired base class is specified as `NotInheritable`. `NotInheritable` classes are used primarily to prevent unintended derivation.  
  
 **Error ID:** BC30299  
  
### To correct this error  
  
-   Remove the `NotInheritable` keyword from the definition of the desired base class, or remove the `Inherits` statement.  
  
## See Also  
 [Inheritance Basics](/dotnet/visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics)   
 [NotInheritable](/dotnet/visual-basic/language-reference/modifiers/notinheritable)   
 [Inherits Statement](/dotnet/visual-basic/language-reference/statements/inherits-statement)