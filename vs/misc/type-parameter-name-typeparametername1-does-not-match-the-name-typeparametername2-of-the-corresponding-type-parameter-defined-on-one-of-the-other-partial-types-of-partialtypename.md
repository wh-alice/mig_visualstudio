---
title: "Type parameter name &#39;&lt;typeparametername1&gt;&#39; does not match the name &#39;&lt;typeparametername2&gt;&#39; of the corresponding type parameter defined on one of the other partial types of &#39;&lt;partialtypename&gt;&#39; | Microsoft Docs"
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
  - "vbc30931"
  - "bc30931"
helpviewer_keywords: 
  - "BC30931"
ms.assetid: 01b053c3-d1b5-4e69-b908-3d5cfc73913b
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
# Type parameter name &#39;&lt;typeparametername1&gt;&#39; does not match the name &#39;&lt;typeparametername2&gt;&#39; of the corresponding type parameter defined on one of the other partial types of &#39;&lt;partialtypename&gt;&#39;
A generic class or structure is defined in multiple partial declarations with conflicting type parameter specifications.  
  
 When you divide the definition of a class or structure among several partial declarations, the compiler treats the type as the union of all its partial declarations. This applies not only to the members but also to the implementation, inheritance, and access level.  
  
 You cannot specify multiple names for any type parameter in the definition of a generic class or structure.  
  
 **Error ID:** BC30931  
  
### To correct this error  
  
-   Decide what name the type parameter should have, and use the same name in every partial declaration.  
  
## See Also  
 [Partial](/dotnet/visual-basic/language-reference/modifiers/partial)   
 [Class Statement](/dotnet/visual-basic/language-reference/statements/class-statement)   
 [Structure Statement](/dotnet/visual-basic/language-reference/statements/structure-statement)   
 [NOT IN BUILD: Classes: Blueprints for Objects](http://msdn.microsoft.com/en-us/2c86373d-0333-4616-a7d8-4790c4e89f7b)   
 [Structures](/dotnet/visual-basic/programming-guide/language-features/data-types/structures)   
 [Generic Types in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-types)   
 [Type List](/dotnet/visual-basic/language-reference/statements/type-list)