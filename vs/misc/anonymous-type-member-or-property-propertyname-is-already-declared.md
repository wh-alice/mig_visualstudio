---
title: "Anonymous type member or property &#39;&lt;propertyname&gt;&#39; is already declared | Microsoft Docs"
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
  - "bc36547"
  - "vbc36547"
helpviewer_keywords: 
  - "BC36547"
ms.assetid: 4c60d24a-62d7-404a-bc35-d1a1d9c9f851
caps.latest.revision: 7
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
# Anonymous type member or property &#39;&lt;propertyname&gt;&#39; is already declared
A property name can be established only once in the declaration of an anonymous type. For example, the following declarations are not valid:  
  
```vb#  
'' Not valid, because the Label property is assigned to twice.  
' Dim anonType1 = New With {.Label = "Debra Garcia", .Label = .Label & ", President"}  
'' Not valid, because the property name inferred for both properties is  
'' Name.  
' Dim anonType2 = New With {Key product.Name, Key car1.Name}  
```  
  
 **Error ID:** BC36547  
  
### To correct this error  
  
-   Choose a different name for one of the properties.  
  
    ```vb#  
    ' Valid.  
    Dim anonType3 = New With {.Name = "Debra Garcia", .Label = .Name & ", President"}  
    ```  
  
-   Provide new names for the variables or property names from which you are inferring names and values.  
  
    ```vb#  
    ' Valid.  
    Dim anonType4 = New With {Key .ProductName = product.Name, Key .CarName = car1.Name}  
  
    ```  
  
## See Also  
 [Anonymous Types](/dotnet/visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types)   
 [How to: Infer Property Names and Types in Anonymous Type Declarations](http://msdn.microsoft.com/en-us/Library/7c748b22-913f-4d9d-b747-6b7bf296a0bc)