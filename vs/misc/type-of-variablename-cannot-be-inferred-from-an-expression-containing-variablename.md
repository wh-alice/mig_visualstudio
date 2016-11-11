---
title: "Type of &#39;&lt;variablename&gt;&#39; cannot be inferred from an expression containing &#39;&lt;variablename&gt;&#39; | Microsoft Docs"
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
  - "vbc30980"
  - "bc30980"
helpviewer_keywords: 
  - "BC30980"
ms.assetid: 43a5d008-5362-481b-845b-b9bb00a61a83
caps.latest.revision: 21
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
# Type of &#39;&lt;variablename&gt;&#39; cannot be inferred from an expression containing &#39;&lt;variablename&gt;&#39;
The compiler cannot infer the data type of a variable if the variable is used in establishing its initial value in the declaration.  
  
 For example, with `Option Infer` set to `On`, the following examples do not compile:  
  
-   Declarations  
  
    ```  
    ' Does not compile with Option Infer on.  
    Dim m = m  
    Dim d = someFunction(d)  
    ```  
  
-   `For` loop  
  
    ```  
    ' Does not compile with Option Infer on.  
    For j = 1 To j  
    Next  
    ```  
  
-   `For Each` loop  
  
    ```  
    ' Does not compile with Option Infer on.  
    For Each customer In customer.Orders  
    Next  
    ```  
  
 **Error ID:** BC30980  
  
### To correct this error  
  
-   If the two variables were intended to refer to different values, change the name of the variable that you are declaring.  
  
-   Use a literal value instead of the variable name in the initial value, on the right side of the assignment.  
  
-   Use an `As` clause to specify the type of the variable you are declaring.  
  
## See Also  
 [Dim Statement](/dotnet/visual-basic/language-reference/statements/dim-statement)   
 [For Each...Next Statement](/dotnet/visual-basic/language-reference/statements/for-each-next-statement)   
 [For...Next Statement](/dotnet/visual-basic/language-reference/statements/for-next-statement)   
 [Local Type Inference](/dotnet/visual-basic/programming-guide/language-features/variables/local-type-inference)   
 [Option Infer Statement](/dotnet/visual-basic/language-reference/statements/option-infer-statement)