---
title: "Local variable &#39;&lt;variablename&gt;&#39; is already declared in the current block | Microsoft Docs"
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
  - "bc30288"
  - "vbc30288"
helpviewer_keywords: 
  - "BC30288"
ms.assetid: 99352028-6c60-4596-9ea8-cdae632fefb8
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
# Local variable &#39;&lt;variablename&gt;&#39; is already declared in the current block
Two variables with the same name are declared in the same block (which can be a procedure or a control block such as `If...Then`).  
  
 **Error ID:** BC30288  
  
### To correct this error  
  
-   Move one of the declarations to a different block, or change the name of one of the variables.  
  
## See Also  
 [NOTINBUILD: Resolving a Reference When Multiple Variables Have the Same Name](http://msdn.microsoft.com/en-us/9601e39f-1911-44e1-ace5-3f6e090408b9)   
 [Shadowing in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/declared-elements/shadowing)