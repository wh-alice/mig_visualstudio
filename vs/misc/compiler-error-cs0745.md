---
title: "Compiler Error CS0745 | testtitle"
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
  - "CS0745"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0745"
ms.assetid: 6ae77eb2-a940-43aa-a198-3042d144613a
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
# Compiler Error CS0745
Expected contextual keyword 'by'  
  
 The pattern for the `group` clause is `group...by` followed by an optional `into`, as shown in the following example:  
  
```  
string[] names = { "Bob", "Bill", "Jonetta", "Mary" };  
  
var query = from name in names  
            group name by name[0];  
```  
  
 or  
  
```  
var query2 = from name in names  
             group name by name[0] into g  
             //...additional query clauses  
```  
  
### To correct this error  
  
1.  Add the `by` keyword to the `group` clause.  
  
## Example  
 The following code generates CS0745:  
  
```  
// cs0745.cs  
using System;  
using System.Linq;  
  
public class C  
{  
    public static int Main()  
    {  
        string[] names = { "Bob", "Bill", "Jonetta", "Mary" };  
  
        var query = from name in names  
                    group name name[0]; // CS0745  
  
        return 1;  
    }  
}  
```  
  
## See Also  
 [LINQ Query Expressions](../Topic/LINQ%20Query%20Expressions%20\(C%23%20Programming%20Guide\).md)   
 [group clause](../Topic/group%20clause%20\(C%23%20Reference\).md)