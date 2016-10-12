---
title: "Instance members and &#39;Me&#39; cannot be used in a query expression"
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
  - "vbc36535"
  - "bc36535"
helpviewer_keywords: 
  - "BC36535"
ms.assetid: afb5281b-70a7-48c7-a46d-39522b96b1ff
caps.latest.revision: 7
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
# Instance members and &#39;Me&#39; cannot be used in a query expression
A LINQ query in a `Structure` includes a reference to `Me` or to an instance member of the structure. References to `Me` or instance members are not allowed in query expressions within a `Structure`.  
  
 **Error ID:** BC36535  
  
### To correct this error  
  
1.  Create a copy of the instance member or the value returned by the reference to `Me` and use the copy in the query expression, as shown in the following example.  
  
    ```vb#  
    Structure SampleStructure  
        Public SearchValue As Integer  
  
        Public Sub SetSearchValue(ByVal number As Integer)  
          SearchValue = number  
        End Sub  
  
        Public Sub GetData()  
            Dim sv = SearchValue  
            Dim SampleData = New Integer() {1, 2, 3, 4}  
            Dim query = From number In SampleData _  
                        Where number < sv  
        End Sub  
    End Structure  
    ```  
  
## See Also  
 [Introduction to LINQ in Visual Basic](../Topic/Introduction%20to%20LINQ%20in%20Visual%20Basic.md)   
 [LINQ](../Topic/LINQ%20in%20Visual%20Basic.md)   
 [Me](assetId:///a65973c7-cf06-4547-9b25-9fba885525c2)   
 [Structure (Visual Basic)](assetId:///263ce115-ac36-4c05-8cb7-0e0eead5c6d0)