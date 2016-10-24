---
title: "Reference to a non-shared member requires an object reference"
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
  - "bc30469"
  - "vbc30469"
helpviewer_keywords: 
  - "BC30469"
ms.assetid: af503e8b-2e1f-4f91-a07f-b1ddd73dd4a6
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
# Reference to a non-shared member requires an object reference
You have referenced a non-shared member within your code and failed to supply an object reference. You cannot use the class name itself to qualify a member that is not shared. The instance must first be declared as an object variable and then referenced by the variable name.  
  
 **Error ID:** BC30469  
  
### To correct this error  
  
1.  Declare the instance as an object variable.  
  
2.  Reference the instance by the variable name.  
  
## See Also  
 [NOT IN BUILD: Understanding Classes](http://msdn.microsoft.com/en-us/cc2355a2-cb98-4353-9440-736585aec46c)   
 [NOT IN BUILD: Shared Members in Visual Basic](http://msdn.microsoft.com/en-us/dbc3783f-83a2-4225-995d-c2d6d025663d)   
 [Shared](../Topic/Shared%20\(Visual%20Basic\).md)   
 [NOTINBUILD: Resolving a Reference When Multiple Variables Have the Same Name](http://msdn.microsoft.com/en-us/9601e39f-1911-44e1-ace5-3f6e090408b9)