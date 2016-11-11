---
title: "Cannot inherit interface &#39;&lt;interfacename1&gt;&#39; because the interface &#39;&lt;interfacename2&gt;&#39; from which it inherits could be identical to interface &#39;&lt;interfacename3&gt;&#39; from which the interface &#39;&lt;interfacename4&gt;&#39; inherits for some type arguments | Microsoft Docs"
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
  - "vbc32122"
  - "bc32122"
helpviewer_keywords: 
  - "BC32122"
ms.assetid: 64a66ec7-0f5f-4804-a92b-9a6279fdfd6d
caps.latest.revision: 5
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
# Cannot inherit interface &#39;&lt;interfacename1&gt;&#39; because the interface &#39;&lt;interfacename2&gt;&#39; from which it inherits could be identical to interface &#39;&lt;interfacename3&gt;&#39; from which the interface &#39;&lt;interfacename4&gt;&#39; inherits for some type arguments
A generic interface inherits from two or more generic interfaces, and two of the inheritances could conflict for certain values of type arguments.  
  
 The following statements can generate this error.  
  
```  
Public Interface interfaceA(Of u)  
End Interface  
Public Interface interfaceX(Of v)  
    Inherits interfaceA(Of v)  
End Interface  
Public Interface interfaceY(Of w)  
    Inherits interfaceA(Of w)  
End Interface  
Public Interface derivedInterface(Of t1, t2)  
    Inherits interfaceX(Of t1), interfaceY(Of t2)  
End Interface  
```  
  
 If `derivedInterface` is constructed or implemented supplying the same type to both `t1` and `t2`, it must inherit two versions of `interfaceA` with identical type arguments. Doing so would produce an ambiguity about which version to access.  
  
 **Error ID:** BC32122  
  
### To correct this error  
  
-   Change one of the type arguments supplied to the derived interface so that there is no conflict.  
  
     -or-  
  
-   Remove from the `Inherits` statement one of the interfaces causing the potential inheritance or implementation conflict.  
  
## See Also  
 [NOT IN BUILD: Interfaces Overview](http://msdn.microsoft.com/en-us/f96bb470-c1b8-4c73-89bc-6f536b798da1)   
 [Interface Statement](/dotnet/visual-basic/language-reference/statements/interface-statement)   
 [Inheritance Basics](/dotnet/visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics)   
 [Inherits Statement](/dotnet/visual-basic/language-reference/statements/inherits-statement)   
 [Generic Types in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-types)