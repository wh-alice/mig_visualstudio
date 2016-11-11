---
title: "Constant cannot be the target of an assignment | Microsoft Docs"
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
  - "bc30074"
  - "vbc30074"
helpviewer_keywords: 
  - "BC30074"
ms.assetid: e805a517-228a-4147-a2c0-9dba93d3ba42
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
# Constant cannot be the target of an assignment
A constant occurs in a context that assigns a value to it. Only writable variables, properties, and array elements can have values assigned to them during execution.  
  
 **Error ID:** BC30074  
  
### To correct this error  
  
-   Replace the constant with a single writable variable, property, or array element.  
  
## See Also  
 [Constants and Enumerations](/dotnet/visual-basic/programming-guide/language-features/constants-enums/index)   
 [NotInBuild:Assignment Statements](http://msdn.microsoft.com/en-us/eb4f91e9-fbbf-45ca-b21d-e8ae069de4f9)