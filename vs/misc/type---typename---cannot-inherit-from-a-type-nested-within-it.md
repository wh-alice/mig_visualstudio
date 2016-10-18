---
title: "Type &#39;&lt;typename&gt;&#39; cannot inherit from a type nested within it"
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
  - "bc30908"
  - "vbc30908"
helpviewer_keywords: 
  - "BC30908"
ms.assetid: bca164b2-a4a9-4ed4-9f71-a9a5a42f181a
caps.latest.revision: 13
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
# Type &#39;&lt;typename&gt;&#39; cannot inherit from a type nested within it
A class or interface definition includes an [Inherits Statement](../Topic/Inherits%20Statement.md) that specifies a type nested within it.  
  
 Inheritance must be linear, not circular. A type cannot inherit from a type that inherits from it.  
  
 A related restriction is that a type cannot inherit from a type that is not yet defined. Inheritance involves the ability to reuse members of the base class, which in turn requires that these members be defined. Therefore, [!INCLUDE[vbprvb](../codequality/includes/vbprvb_md.md)] cannot compile code such as the following example.  
  
```  
Public Class outerClass  
    ' The following statement is INVALID because innerClass is not defined.  
    Inherits innerClass  
    Public Class innerClass  
        Public Sub doSomething()  
        End Sub  
    End Class  
End Class  
```  
  
 **Error ID:** BC30908  
  
### To correct this error  
  
-   If the inheriting type (the outer type in the nesting) must inherit from the inner type, move the inner type out of the outer type.  
  
-   If the inner type must be nested within the outer type, the outer type cannot inherit from it. Remove the [Inherits Statement](../Topic/Inherits%20Statement.md).  
  
## See Also  
 [NOT IN BUILD: Inheritance in Visual Basic](http://msdn.microsoft.com/en-us/e5e6e240-ed31-4657-820c-079b7c79313c)