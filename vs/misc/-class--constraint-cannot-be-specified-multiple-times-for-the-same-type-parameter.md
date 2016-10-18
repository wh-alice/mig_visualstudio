---
title: "&#39;Class&#39; constraint cannot be specified multiple times for the same type parameter"
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
  - "bc32101"
  - "vbc32101"
helpviewer_keywords: 
  - "BC32101"
ms.assetid: fac2330a-e397-4bd9-8166-934407575f9e
caps.latest.revision: 8
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
# &#39;Class&#39; constraint cannot be specified multiple times for the same type parameter
A constraint list includes the [Class (Visual Basic)](http://msdn.microsoft.com/en-us/0777c6e6-46bc-451b-ad70-57b49d4ef4f7) constraint more than once.  
  
 A constraint list on a type parameter can specify that the type argument passed to that type parameter must be a value type (with the [Structure (Visual Basic)](http://msdn.microsoft.com/en-us/263ce115-ac36-4c05-8cb7-0e0eead5c6d0) constraint) or must be a reference type (with the `Class` constraint). You cannot specify both constraints on the same type parameter, and you cannot specify either one more than once.  
  
 Error ID: BC32101  
  
### To correct this error  
  
-   Remove any redundant `Class` keywords. You should have only one in the constraint list.  
  
## See Also  
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Value Types and Reference Types](../Topic/Value%20Types%20and%20Reference%20Types.md)