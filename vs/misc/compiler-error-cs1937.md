---
title: "Compiler Error CS1937 | testtitle"
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
  - "CS1937"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1937"
ms.assetid: f13e8dc9-8c20-477e-8b74-7192848e08a2
caps.latest.revision: 5
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
# Compiler Error CS1937
The name 'name' is not in scope on the left side of 'equals'. Consider swapping the expressions on either side of 'equals'.  
  
 The `equals` keyword is a special operator that is used in a `join` clause to determine equality between two expressions. The range variable for the left side source sequence is in scope on the left side of equals, and the range variable for the right side source is only in scope on the left side of equals. You can verify this by experimenting with IntelliSense in the following code example.  
  
### To correct this error  
  
1.  Swap the position of the two range variables as shown in the commented line in the following example:  
  
## Example  
 The following example generates CS1937.  
  
```  
// cs1937.cs  
using System.Linq;  
class Test  
{  
    static void Main()  
    {  
        int[] sourceA = { 1, 2, 3, 4, 5 };  
        int[] sourceB = { 3, 4, 5, 6, 7 };  
  
        var query = from a in sourceA  
                    join b in sourceB on b equals a // CS1937  
                    // Try the following line instead.  
                    //join b in sourceB on a equals b  
                    select new { a, b };  
    }  
}  
```  
  
 The left side is generally called the "outer" side and the right is generally called the "inner" side.  
  
## See Also  
 [join clause](../Topic/join%20clause%20\(C%23%20Reference\).md)