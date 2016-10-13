---
title: "Type &#39;&lt;typename&gt;&#39; must define operator &#39;&lt;operator&gt;&#39; to be used in a &#39;For&#39; statement"
ms.custom: na
ms.date: "10/01/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "vbc33038"
  - "BC33038"
helpviewer_keywords: 
  - "BC33038"
ms.assetid: b1c9d87f-80f9-4c8c-8908-f8400b9fe4c5
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
# Type &#39;&lt;typename&gt;&#39; must define operator &#39;&lt;operator&gt;&#39; to be used in a &#39;For&#39; statement
A `For` loop specifies a counter variable of a type that does not support a required operator.  
  
 The counter variable in a `For` loop can be of any data type that supports all of the following operators:  
  
-   Greater than or equal (`>=`)  
  
-   Less than or equal (`<=`)  
  
-   Addition (`+`)  
  
-   Subtraction (`-`)  
  
 If you use a numeric data type for the counter variable, all the preceding operators are supported. If you use a user-defined class or structure, you must define all the preceding operators on that class or structure.  
  
 Note also that the data types of the `start`, `end`, and `step` expressions in the `For` statement must widen to the data type of the counter variable. If the counter variable is a user-defined class or structure and the `start`, `end`, or `step` expression is of a different type, you must define the `CType` conversion operator to accomplish the necessary conversion.  
  
 **Error ID:** BC33038  
  
### To correct this error  
  
1.  Make sure the spelling of the counter-variable data type is correct.  
  
2.  If you are using a user-defined class or structure for the counter variable, define all the required operators on that class or structure.  
  
3.  Depending on the data types of the `start`, `end`, and `step` expressions, you might have to define one or more `CType` conversion operators to convert them to the counter variable data type.  
  
## See Also  
 [For...Next Statement](../Topic/For...Next%20Statement%20\(Visual%20Basic\).md)   
 [Operator Procedures](../Topic/Operator%20Procedures%20\(Visual%20Basic\).md)   
 [Operator Statement](../Topic/Operator%20Statement.md)   
 [How to: Define an Operator](../Topic/How%20to:%20Define%20an%20Operator%20\(Visual%20Basic\).md)   
 [How to: Define a Conversion Operator](../Topic/How%20to:%20Define%20a%20Conversion%20Operator%20\(Visual%20Basic\).md)   
 [CType Function](../Topic/CType%20Function%20\(Visual%20Basic\).md)