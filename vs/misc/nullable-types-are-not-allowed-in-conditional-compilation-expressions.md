---
title: "Nullable types are not allowed in conditional compilation expressions | Microsoft Docs"
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
  - "bc33111"
  - "vbc33111"
helpviewer_keywords: 
  - "BC33111"
ms.assetid: 2c2587e5-2179-4a31-bcf7-7004db6f2d73
caps.latest.revision: 5
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
# Nullable types are not allowed in conditional compilation expressions
A nullable type cannot be used in the expression of a conditional compilation directive. For example, the following code causes this error.  
  
```vb#  
'#Const triggerPoint = 0  
  
'' Not valid.  
'#If CType(triggerpoint, Boolean?) = True Then  
'        ' Body of the conditional directive.  
'#End If  
```  
  
 **Error ID:** BC33111  
  
### To correct this error  
  
-   Remove the nullable type designation.  
  
## See Also  
 [Nullable Value Types](/dotnet/visual-basic/programming-guide/language-features/data-types/nullable-value-types)   
 [#If...Then...#Else Directives](/dotnet/visual-basic/language-reference/directives/if-then-else-directives)   
 [Conditional Compilation](/dotnet/visual-basic/programming-guide/program-structure/conditional-compilation)