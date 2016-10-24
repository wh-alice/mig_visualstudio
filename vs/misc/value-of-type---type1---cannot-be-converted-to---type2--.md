---
title: "Value of type &#39;&lt;type1&gt;&#39; cannot be converted to &#39;&lt;type2&gt;&#39;"
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
  - "bc30311"
  - "vbc30311"
helpviewer_keywords: 
  - "BC30311"
ms.assetid: e3a513d4-2a1e-46d6-b592-b2e756b89d7d
caps.latest.revision: 8
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
# Value of type &#39;&lt;type1&gt;&#39; cannot be converted to &#39;&lt;type2&gt;&#39;
A statement attempts to convert one data type to another in a way that is not defined. Possible causes of this error include the following:  
  
-   A conversion specifies two data types between which no conversion exists. An example of this is a conversion from a `Boolean` value to the `Date` type.  
  
-   An initialization of an array does not include braces (`{}`) following a `New` clause. In this case, \<type2> is of the form '1-dimensional array of \<type>'.  
  
 **Error ID:** BC30311  
  
### To correct this error  
  
-   Make sure the expression can be converted to the destination data type.  
  
-   If \<type2> is an array, make sure the `New` clause contains both parentheses and braces following the type name. The following code illustrates correct initialization of an array.  
  
    ```  
    Dim anIntArray As Integer() = New Integer() {}  
    ```  
  
## See Also  
 [Type Conversions in Visual Basic](../Topic/Type%20Conversions%20in%20Visual%20Basic.md)   
 [How to: Initialize an Array Variable in Visual Basic](../Topic/How%20to:%20Initialize%20an%20Array%20Variable%20in%20Visual%20Basic.md)