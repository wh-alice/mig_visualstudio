---
title: "Compiler Error CS0747 | hehe"
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
  - "CS0747"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0747"
ms.assetid: dc1b7e38-cee5-406c-b193-a60ec4faebe1
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
# Compiler Error CS0747
Invalid initializer member declarator.  
  
 An object initializer is used to assign values to properties or fields. Any expression which is not an assignment to a property or field is a compile-time error.  
  
### To correct this error  
  
1.  Ensure that all expressions in the initializer are assignments to properties or fields of the type. In the following example, the second expression is an error because the value `1` is not assigned to any property or field of `List<int>`.  
  
## Example  
 The following code generates CS0747:  
  
```  
// cs0747.cs  
using System.Collections.Generic;  
  
public class C  
{  
    public static int Main()  
    {  
        var t = new List<int> { Capacity = 2, 1 }; // CS0747  
        return 1;  
    }  
}  
```  
  
## See Also  
 [Object and Collection Initializers](../Topic/Object%20and%20Collection%20Initializers%20\(C%23%20Programming%20Guide\).md)