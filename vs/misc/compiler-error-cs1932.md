---
title: "Compiler Error CS1932"
ms.custom: ""
ms.date: "10/25/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS1932"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1932"
ms.assetid: fc927899-2d35-4d47-9ae9-8fc99295bb66
caps.latest.revision: 6
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
# Compiler Error CS1932
Cannot assign 'expression' to a range variable.  
  
 The compiler must be able to infer the type of a range variable, whether it is introduced in a `from` clause or a `let` clause. It cannot be null because null is not a type, and it cannot be assigned with an expression of an unsafe type.  
  
### To correct this error  
  
-   Remove the assignment that is not valid.  
  
-   Explicitly cast the expression to an allowed type  
  
## Example  
 The following code generates CS1932 because the type of the range variable cannot be inferred. Cast the value to the intended type to fix the error, as shown in the following example.  
  
```  
// CS1932.cs  
using System.Linq;  
class Test  
{  
    static void Main()  
    {  
  
        var x = from i in Enumerable.Range(1, 100)  
                let k = null // CS1932  
                // Try the following line instead.  
                let k = (string) null  
                select i;  
    }  
}  
```  
  
## See Also  
 [LINQ Query Expressions](../Topic/LINQ%20Query%20Expressions%20\(C%23%20Programming%20Guide\).md)