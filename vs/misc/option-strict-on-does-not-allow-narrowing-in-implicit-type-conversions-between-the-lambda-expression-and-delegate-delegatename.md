---
title: "Option Strict On does not allow narrowing in implicit type conversions between the lambda expression and delegate &#39;&lt;delegatename&gt;&#39; | Microsoft Docs"
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
  - "bc36662"
  - "vbc36662"
helpviewer_keywords: 
  - "BC36662"
ms.assetid: 4504497b-56ba-4631-ad7b-59975f7fee04
caps.latest.revision: 4
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
# Option Strict On does not allow narrowing in implicit type conversions between the lambda expression and delegate &#39;&lt;delegatename&gt;&#39;
With `Option Strict` on, you cannot have a narrowing conversion between the data type of a parameter in a delegate and the corresponding parameter of a lambda expression assigned to a variable of that delegate type. For example, in the following code, delegate `Del` has one parameter of type `Integer`.  
  
```vb#  
Delegate Function Del(ByVal p As Integer) As String  
```  
  
 Therefore, the corresponding parameter of any lambda expression assigned to a variable of type `Del` can be an `Integer` or any data type for which there is a widening conversion from `Integer`.  
  
```vb#  
' Valid.  
Dim example1 As Del = Function(n As Integer) "Valid"  
Dim example2 As Del = Function(n As Long) "Valid"  
  
' Not valid.  
Dim example3 As Del = Function(n As Short) "Not Valid"  
```  
  
 **Error ID:** BC36662  
  
### To correct this error  
  
-   Change the data type of the parameter in the delegate or the lambda expression so that the required widening relationship exists.  
  
-   Do not specify parameter data types in the lambda expression. Types will be inferred from the corresponding parameters in the delegate.  
  
    ```vb#  
    Dim example4 As Del = Function(n) "Valid"  
    ```  
  
## See Also  
 [Lambda Expressions](/dotnet/visual-basic/language-reference/procedures/lambda-expressions)   
 [Delegates](/dotnet/visual-basic/programming-guide/language-features/delegates/delegates)   
 [Widening and Narrowing Conversions](/dotnet/visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions)   
 [Relaxed Delegate Conversion](/dotnet/visual-basic/programming-guide/language-features/delegates/relaxed-delegate-conversion)