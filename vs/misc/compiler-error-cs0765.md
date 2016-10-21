---
title: "Compiler Error CS0765"
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
  - "CS0765"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0765"
ms.assetid: adfb1f95-f7b1-4e43-83c2-42e8531eb980
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
# Compiler Error CS0765
Partial methods with only a defining declaration or removed conditional methods cannot be used in expression trees  
  
 Although a call to a removed partial method is an expression, it is not an acceptable expression in an expression tree.  
  
### To correct this error  
  
1.  Add an implementing declaration for the partial method, or remove the code that is causing the conditional method to be excluded from compilation.  
  
## Example  
 The following code generates CS0765 in two locations:  
  
```  
// cs0765.cs  
using System;  
using System.Collections;  
using System.Collections.Generic;  
using System.Diagnostics;  
using System.Linq;  
using System.Linq.Expressions;  
  
public delegate void dele();  
  
public class ConClass  
{  
    [Conditional("CONDITION")]  
    public static void TestMethod() { }  
}  
  
public partial class PartClass : IEnumerable  
{  
    List<object> list = new List<object>();  
  
    partial void Add(int x);  
  
    public IEnumerator GetEnumerator()  
    {  
        for (int i = 0; i < list.Count; i++)  
            yield return list[i];  
    }  
  
    static void Main()  
    {  
        Expression<Func<PartClass>> testExpr1 = () => new PartClass { 1, 2 }; // CS0765  
        Expression<dele> testExpr2 = () => ConClass.TestMethod(); // CS0765  
    }  
}  
```  
  
## See Also  
 [Partial Classes and Methods](../Topic/Partial%20Classes%20and%20Methods%20\(C%23%20Programming%20Guide\).md)   
 [Expression Trees](../Topic/Expression%20Trees%20\(C%23%20and%20Visual%20Basic\).md)