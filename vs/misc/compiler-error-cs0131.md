---
title: "Compiler Error CS0131"
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
  - "CS0131"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0131"
ms.assetid: 822852cc-a426-4b7d-b2ff-0026a0c0a0e7
caps.latest.revision: 10
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
# Compiler Error CS0131
The left-hand side of an assignment must be a variable, property or indexer  
  
 In an assignment statement, the value of the right-hand side is assigned to the left-hand side. The left-hand side must be a variable, property, or indexer.  
  
 To fix this error, make sure that all operators are on the right-hand side and that the left-hand side is a variable, property, or indexer. For more information, see [Statements, Expressions, and Operators](../Topic/Statements,%20Expressions,%20and%20Operators%20\(C%23%20Programming%20Guide\).md).  
  
## Example  
 The following sample generates CS0131.  
  
```  
// CS0131.cs  
public class MyClass  
{  
    public int i = 0;  
    public void MyMethod()  
    {  
        i++ = 1;   // CS0131  
        // try the following line instead  
        // i = 1;  
    }  
    public static void Main() { }  
}  
```  
  
## Example  
 This error can also occur if you attempt to perform arithmetic operations on the left hand side of an assignment operator, as in the following example.  
  
```  
// CS0131b.cs  
public class C  
{  
    public static int Main()  
    {  
        int a = 1, b = 2, c = 3;  
        if (a + b = c) // CS0131  
        // try this instead  
        // if (a + b == c)  
            return 0;  
        return 1;  
    }  
}  
```