---
title: "Member &#39;&lt;membername&gt;&#39; conflicts with member &#39;&lt;membername&gt;&#39; in the base type &#39;&lt;basetypename&gt;&#39; and so should not be declared &#39;Overloads&#39; | Microsoft Docs"
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
  - "bc40021"
  - "vbc40021"
helpviewer_keywords: 
  - "BC40021"
ms.assetid: 2ec72726-ab0e-4545-9c1e-2409eb54482e
caps.latest.revision: 10
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
# Member &#39;&lt;membername&gt;&#39; conflicts with member &#39;&lt;membername&gt;&#39; in the base type &#39;&lt;basetypename&gt;&#39; and so should not be declared &#39;Overloads&#39;
A property or procedure uses the [Overloads](/dotnet/visual-basic/language-reference/modifiers/overloads) keyword to redeclare an existing property or procedure with the same name, but the existing property or procedure is in the base class.  
  
 Overloading is used to define multiple versions of a property or procedure all in the same class. You cannot define an additional version of a base class member unless the base class member already specifies [Overloads](/dotnet/visual-basic/language-reference/modifiers/overloads).  
  
 By default, this message is a warning. For more information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../ide/configuring-warnings-in-visual-basic.md).  
  
 **Error ID:** BC40021  
  
### To correct this error  
  
-   If you intend to define an additional version of the base class member and have access to the source code of the base class, add the [Overloads](/dotnet/visual-basic/language-reference/modifiers/overloads) keyword to the base class definition.  
  
-   If you do not have access to the source code of the base class, you cannot overload the member in a derived class. Remove the `Overloads` keyword.  
  
-   If you wish to replace the base class member instead of defining an additional version of it, use the [Overrides](/dotnet/visual-basic/language-reference/modifiers/overrides) keyword instead of `Overloads`.  
  
-   If you wish to hide the base class member with a new member in the derived class, use the [Shadows](/dotnet/visual-basic/language-reference/modifiers/shadows) keyword instead of `Overloads`.  
  
## See Also  
 [Procedure Overloading](/dotnet/visual-basic/language-reference/procedures/procedure-overloading)   
 [Inheritance Basics](/dotnet/visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics)