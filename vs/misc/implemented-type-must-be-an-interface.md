---
title: "Implemented type must be an interface | Microsoft Docs"
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
  - "bc30232"
  - "vbc30232"
helpviewer_keywords: 
  - "BC30232"
ms.assetid: 63f3dd4c-2f99-4070-b506-2fa808df24d4
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
# Implemented type must be an interface
An `Implements` statement does not specify an interface. A class can implement only an interface.  
  
 **Error ID:** BC30232  
  
### To correct this error  
  
1.  Ensure that the interface name is spelled correctly.  
  
2.  If the statement specifies a class, consider using the `Inherits` statement.  
  
## See Also  
 [Implements Statement](/dotnet/visual-basic/language-reference/statements/implements-statement)   
 [Inherits Statement](/dotnet/visual-basic/language-reference/statements/inherits-statement)   
 [NOT IN BUILD: Inheritance in Visual Basic](http://msdn.microsoft.com/en-us/e5e6e240-ed31-4657-820c-079b7c79313c)