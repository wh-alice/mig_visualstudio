---
title: "Inappropriate use of &lt;keyword&gt; keyword in a module"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc42028"
  - "BC42028"
helpviewer_keywords: 
  - "BC42028"
ms.assetid: a9bc1e9d-ba2c-4a71-b147-0fb66f670316
caps.latest.revision: 12
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
# Inappropriate use of &lt;keyword&gt; keyword in a module
Modules do not have instances, support inheritance, or implement interfaces. Therefore, the following keywords do not apply to a module declaration:  
  
-   [MustInherit](../Topic/MustInherit%20\(Visual%20Basic\).md)  
  
-   [NotInheritable](../Topic/NotInheritable%20\(Visual%20Basic\).md)  
  
-   [Overloads](../Topic/Overloads%20\(Visual%20Basic\).md)  
  
-   [Private](../Topic/Private%20\(Visual%20Basic\).md)  
  
-   [Protected](../Topic/Protected%20\(Visual%20Basic\).md)  
  
-   [Shadows](../Topic/Shadows%20\(Visual%20Basic\).md)  
  
-   [Shared](../Topic/Shared%20\(Visual%20Basic\).md)  
  
-   [Static](../Topic/Static%20\(Visual%20Basic\).md)  
  
 The only keywords supported in a [Module Statement](../Topic/Module%20Statement.md) are [Public](../Topic/Public%20\(Visual%20Basic\).md) and [Friend](../Topic/Friend%20\(Visual%20Basic\).md).  
  
 In addition, you cannot use the [Implements](../Topic/Implements%20Clause%20\(Visual%20Basic\).md) statement or the [Inherits Statement](../Topic/Inherits%20Statement.md) in the statement block of the module.  
  
 By default, this message is a warning. For more information about how to hide warnings or treat warnings as errors, see [Configuring Warnings in Visual Basic](../ide/configuring-warnings-in-visual-basic.md).  
  
 **Error ID:** BC42028  
  
### To correct this error  
  
-   If you intend this programming element to be a module, use only the `Public` or `Friend` keyword in its declaration. By default, a module uses to `Friend` if you do not specify its access level.  
  
-   If you intend to create instances of this programming element, declare it as a class. You can then use the keywords that apply to a class declaration.  
  
## See Also  
 [Class Statement](../Topic/Class%20Statement%20\(Visual%20Basic\).md)