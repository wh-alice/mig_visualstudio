---
title: "Compiler Error CS1920 | hehe"
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
  - "CS1920"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1920"
ms.assetid: efb4782f-a222-4fb5-9e79-8bd2d380520b
caps.latest.revision: 6
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
# Compiler Error CS1920
Element initializer cannot be empty.  
  
 A collection initializer consists of a sequence of element initializers. The element initializers do not have to be enclosed in braces unless they contain an assignment expression. However, if you do supply braces, they cannot be empty. If the element initializer is an object initializer, the braces may be empty as long as the initializer contains a new object creation expression.  
  
### To correct this error  
  
-   Add the missing expression between the braces.  
  
-   If the expression is intended to be an object initializer, add the new object creation expression in front of the braces.  
  
## Example  
 The following example generates CS1920:  
  
```  
  // cs1920.cs  
using System.Collections.Generic;  
public class Test  
{  
    public static int Main()  
    {  
        // Error. Empty initializer   
        // for inner list.  
        List<List<int>> collection =  
            new List<List<int>>() { { } }; // CS1920  
  
        // OK. No initializer for inner list.  
        List<List<int>> collection2 =  
            new List<List<int>>() {  };  
  
        // OK. Inner list is initialized   
        // to one List<int> with zero elements.  
        List<List<int>> collection3 =  
            new List<List<int>>() { new List<int> { } };  
        return 0;  
    }  
}  
```  
  
## See Also  
 [Object and Collection Initializers](../Topic/Object%20and%20Collection%20Initializers%20\(C%23%20Programming%20Guide\).md)