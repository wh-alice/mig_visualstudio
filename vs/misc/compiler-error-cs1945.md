---
title: "Compiler Error CS1945 | testtitle"
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
  - "CS1945"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1945"
ms.assetid: 787f61b0-4767-451c-8c78-8e456b5057eb
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
# Compiler Error CS1945
An expression tree may not contain an anonymous method expression.  
  
 Expression trees can only contain expressions. Anonymous methods can only represent statements.  
  
### To correct this error  
  
1.  Do not try to create an expression tree with a statement.  
  
## Example  
 The following code generates CS1945:  
  
```  
// cs1945.cs  
using System;  
using System.Linq.Expressions;  
  
public delegate void D();  
class Test  
{  
    static void Main()  
    {  
        Expression<Func<int, Func<int, bool>>> tree = (x => delegate(int i) { return true; }); // CS1945  
    }  
}  
```  
  
## See Also  
 [Expression Trees](../Topic/Expression%20Trees%20\(C%23%20and%20Visual%20Basic\).md)   
 [Statements, Expressions, and Operators](../Topic/Statements,%20Expressions,%20and%20Operators%20\(C%23%20Programming%20Guide\).md)