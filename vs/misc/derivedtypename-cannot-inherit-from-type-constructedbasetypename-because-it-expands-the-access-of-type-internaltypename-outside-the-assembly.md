---
title: "&#39;&lt;derivedtypename&gt;&#39; cannot inherit from &lt;type&gt; &#39;&lt;constructedbasetypename&gt;&#39; because it expands the access of type &#39;&lt;internaltypename&gt;&#39; outside the assembly | Microsoft Docs"
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
  - "BC30922"
  - "vbc30922"
helpviewer_keywords: 
  - "BC30922"
ms.assetid: 81909654-7e67-4b89-81a3-25ae57f678f7
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
# &#39;&lt;derivedtypename&gt;&#39; cannot inherit from &lt;type&gt; &#39;&lt;constructedbasetypename&gt;&#39; because it expands the access of type &#39;&lt;internaltypename&gt;&#39; outside the assembly
A derived class or interface attempts to expand the access level of a restricted type by using it as a type argument to a base class or interface.  
  
 The following code can generate this error.  
  
```  
Public Class baseClass(Of t)  
End Class  
Public Class derivedClass  
    Inherits baseClass(Of restrictedStructure)  
End Class  
Friend Structure restrictedStructure  
    Dim firstMember As Integer  
End Structure  
```  
  
 Code outside the assembly is not allowed to access `restrictedStructure`. However, `derivedClass` can be accessed from any code that can reference it. Therefore, `derivedClass` cannot inherit `baseClass` if it uses `restrictedStructure` as a type argument, because that could expose `restrictedStructure` to code in any assembly.  
  
 **Error ID:** BC30922  
  
### To correct this error  
  
-   Adjust the access levels of the classes or interfaces so the derived type does not expand the access level of the restricted type.  
  
     -or-  
  
-   If you cannot adjust the access levels, do not use the restricted type as a type argument when constructing the base class or interface.  
  
## See Also  
 [Inherits Statement](/dotnet/visual-basic/language-reference/statements/inherits-statement)   
 [Inheritance Basics](/dotnet/visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics)   
 [Access Levels in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/declared-elements/access-levels)   
 [Generic Types in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-types)   
 [Type List](/dotnet/visual-basic/language-reference/statements/type-list)