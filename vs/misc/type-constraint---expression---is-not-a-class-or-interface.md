---
title: "Type constraint &#39;&lt;expression&gt;&#39; is not a class or interface"
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
  - "bc32048"
  - "vbc32048"
helpviewer_keywords: 
  - "BC32048"
ms.assetid: 68811886-44ac-43e1-9315-b39857310033
caps.latest.revision: 10
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
# Type constraint &#39;&lt;expression&gt;&#39; is not a class or interface
A constraint list includes an expression that does not represent a valid constraint on a type parameter.  
  
 A constraint list imposes requirements on the type argument passed to the type parameter. You can specify the following requirements in any combination:  
  
-   The type argument must implement one or more interfaces  
  
-   The type argument must inherit from at most one class  
  
-   The type argument must expose a parameterless constructor that the creating code can access  
  
-   The type argument must be a reference type, or it must be a value type  
  
 **Error ID:** BC32048  
  
### To correct this error  
  
-   Verify that the expression and its elements are spelled correctly.  
  
-   If the expression does not qualify for the preceding list of requirements, remove it from the constraint list.  
  
-   If the expression refers to an interface or class, verify that the compiler has access to that interface or class. You might need to qualify its name, and you might need to add a reference to your project. For more information, see "References to Projects" in [NOTINBUILD: Resolving a Reference When Multiple Variables Have the Same Name](http://msdn.microsoft.com/9601e39f-1911-44e1-ace5-3f6e090408b9).  
  
## See Also  
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Value Types and Reference Types](../Topic/Value%20Types%20and%20Reference%20Types.md)   
 [NOTINBUILD  How to: Qualify a Declared Element Name](http://msdn.microsoft.com/6bd112f5-df6f-42b8-9427-a9225bfcbaab)   
 [How to: Add and Remove Project References](http://msdn.microsoft.com/f51b784d-0bc8-4c19-a898-e560d5ed696b)