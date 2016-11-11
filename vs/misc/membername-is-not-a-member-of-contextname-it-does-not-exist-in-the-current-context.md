---
title: "&#39;&lt;membername&gt;&#39; is not a member of &#39;&lt;contextname&gt;&#39;; it does not exist in the current context | Microsoft Docs"
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
  - "vbc36557"
  - "bc36557"
helpviewer_keywords: 
  - "BC36557"
ms.assetid: d8671f1c-d545-44da-89b3-7d892e01e8be
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
# &#39;&lt;membername&gt;&#39; is not a member of &#39;&lt;contextname&gt;&#39;; it does not exist in the current context
A non-existent member name has been assigned to a property in an anonymous type declaration. In the following example, `.Prop1` and `.Prop2` are the properties of the anonymous type. The attempt to assign `.Prop3` to `.Prop2` causes the error.  
  
```vb#  
' Not valid.  
Dim anon1 = New With {.Prop1 = 27, .Prop2 = .Prop3}  
  
' The assignment is valid if the assigned property has been declared   
' and initialized.  
Dim anon2 = New With {.Prop1 = 27, .Prop2 = .Prop1}  
```  
  
 **Error ID:** BC36657  
  
### To correct this error  
  
-   Examine your code to determine what you want to assign. The variable name might be misspelled, or it might require qualification if it is a property of another object.  
  
## See Also  
 [Anonymous Types](/dotnet/visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types)   
 [How to: Infer Property Names and Types in Anonymous Type Declarations](../Topic/How%20to:%20Infer%20Property%20Names%20and%20Types%20in%20Anonymous%20Type%20Declarations%20\(Visual%20Basic\).md)