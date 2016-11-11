---
title: "Constructors cannot implement interface methods | Microsoft Docs"
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
  - "bc30550"
  - "vbc30550"
helpviewer_keywords: 
  - "BC30550"
ms.assetid: 982a767d-9174-408e-bdcf-ae0d96f88cef
caps.latest.revision: 8
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
# Constructors cannot implement interface methods
You have attempted to use the `New` keyword to implement an interface method, which is not valid.  
  
 **Error ID:** BC30550  
  
### To correct this error  
  
-   Implement interfaces with the `Implements` keyword.  
  
## See Also  
 [Implements Statement](/dotnet/visual-basic/language-reference/statements/implements-statement)   
 [NOT IN BUILD: Interfaces Overview](http://msdn.microsoft.com/en-us/f96bb470-c1b8-4c73-89bc-6f536b798da1)