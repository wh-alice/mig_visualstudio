---
title: "Compiler Error CS0742 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0742"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0742"
ms.assetid: 078ee7af-17e4-4572-8fee-d97e09c9002b
caps.latest.revision: 7
author: "BillWagner"
ms.author: "wiwagn"
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
# Compiler Error CS0742
A query body must end with a select clause or a group clause  
  
 A query expression must terminate with either a `select` clause or a `group` clause without a continuation.  
  
### To correct this error  
  
1.  Add a [select clause](/dotnet/csharp/language-reference/keywords/select-clause) or [group clause](/dotnet/csharp/language-reference/keywords/group-clause) to the query.  
  
## Example  
 The following code generates CS0742:  
  
```  
// cs0742.cs  
using System.Linq;  
public class Test  
{  
    public static int Main()  
    {  
        int[] array = { 1, 2, 3 };  
        var query = from num in array; // CS0742  
        return 1;  
    }  
}  
```  
  
 If the `group` clause uses the [into](/dotnet/csharp/language-reference/keywords/into) keyword to store the results of the grouping into a temporary identifier, it cannot be the last clause in a query. A `select` or second `group` clause is still required.  
  
## See Also  
 [LINQ Query Expressions](/dotnet/csharp/programming-guide/linq-query-expressions/index)