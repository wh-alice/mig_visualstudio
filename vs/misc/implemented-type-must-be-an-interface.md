---
title: "Implemented type must be an interface | hehe"
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
  - "bc30232"
  - "vbc30232"
helpviewer_keywords: 
  - "BC30232"
ms.assetid: 63f3dd4c-2f99-4070-b506-2fa808df24d4
caps.latest.revision: 9
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
# Implemented type must be an interface
An `Implements` statement does not specify an interface. A class can implement only an interface.  
  
 **Error ID:** BC30232  
  
### To correct this error  
  
1.  Ensure that the interface name is spelled correctly.  
  
2.  If the statement specifies a class, consider using the `Inherits` statement.  
  
## See Also  
 [Implements Statement](../Topic/Implements%20Statement.md)   
 [Inherits Statement](../Topic/Inherits%20Statement.md)   
 [NOT IN BUILD: Inheritance in Visual Basic](http://msdn.microsoft.com/en-us/e5e6e240-ed31-4657-820c-079b7c79313c)