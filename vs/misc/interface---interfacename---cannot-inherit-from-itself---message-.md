---
title: "Interface &#39;&lt;interfacename&gt;&#39; cannot inherit from itself: &lt;message&gt;"
ms.custom: na
ms.date: "10/13/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "vbc30296"
  - "BC30296"
helpviewer_keywords: 
  - "BC30296"
ms.assetid: a5bc1ae2-2083-4e26-b8a4-3c4dd951fd27
caps.latest.revision: 11
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
# Interface &#39;&lt;interfacename&gt;&#39; cannot inherit from itself: &lt;message&gt;
An [Inherits Statement](../Topic/Inherits%20Statement.md) in an interface definition specifies its own interface.  
  
 An interface can inherit from another interface, which provides it with all the members of the interface it inherits from, so it does not have to define those members again. Such an interface is called a *derived interface*, and the interface it inherits from is called the *base interface*.  
  
 It is meaningless for an interface to inherit from itself, because it already possesses all its own members.  
  
 **Error ID:** BC30296  
  
### To correct this error  
  
1.  Check the spelling of the interface name in the `Inherits` statement.  
  
2.  If you do not intend to inherit from a different interface, remove the `Inherits` statement entirely.  
  
3.  Examine the cited message for suggestions.  
  
## See Also  
 [NOT IN BUILD: Inheritance in Visual Basic](http://msdn.microsoft.com/en-us/e5e6e240-ed31-4657-820c-079b7c79313c)   
 [Interfaces](../Topic/Interfaces%20\(Visual%20Basic\).md)