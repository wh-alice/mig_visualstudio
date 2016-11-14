---
title: "&#39;}&#39; expected | Microsoft Docs"
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
  - "vbc30370"
  - "bc30370"
helpviewer_keywords: 
  - "BC30370"
ms.assetid: a4ce9be9-fc5d-46ec-a217-c3428bd0b97e
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
# &#39;}&#39; expected
An array initializer or a constraint list has not been ended in a valid fashion.  
  
 The element values with which to initialize an array must be enclosed in braces (`{}`).  
  
```  
Dim demoArray() As Integer = New Integer() {1, 2, 3}   
```  
  
 Similarly, the constraints in a constraint list for a generic type parameter must be enclosed in braces.  
  
```  
Public Class dictionaryMaker(Of t As {IComparable, IDisposable, New})   
```  
  
 **Error ID:** BC30370  
  
### To correct this error  
  
-   Use "}" to end the array initializer or constraint list.  
  
## See Also  
 [Arrays](/dotnet/visual-basic/programming-guide/language-features/arrays/index)   
 [How to: Initialize an Array Variable in Visual Basic](http://msdn.microsoft.com/en-us/Library/aadd7a60-7ca4-4608-b986-091f19e7fc10)   
 [Type List](/dotnet/visual-basic/language-reference/statements/type-list)   
 [Generic Types in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-types)