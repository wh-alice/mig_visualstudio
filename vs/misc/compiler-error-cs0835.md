---
title: "Compiler Error CS0835 | Microsoft Docs"
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
  - "CS0835"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0835"
ms.assetid: 593c26f6-6d82-49a6-8ace-4d29dd9f5fbe
caps.latest.revision: 8
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
# Compiler Error CS0835
Cannot convert lambda to an expression tree whose type argument 'type' is not a delegate type.  
  
 If a lambda expression is converted to an expression tree, the expression tree must have a delegate type for its argument. Furthermore, the lambda expression must be convertible to the delegate type.  
  
### To correct this error  
  
1.  Change the type parameter from `int` to a delegate type, for example `Func<int,int>`.  
  
## Example  
 The following example generates CS0835:  
  
```  
// cs0835.cs  
using System;  
using System.Linq;  
using System.Linq.Expressions;  
  
public class C  
{  
    public static int Main()  
    {  
        Expression<int> e = x => x + 1; // CS0835  
  
        // Try the following line instead.  
       // Expression<Func<int,int>> e2 = x => x + 1;  
  
        return 1;  
    }  
}  
```