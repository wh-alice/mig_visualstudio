---
title: "Compiler Error CS0027 | hehe"
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
  - "CS0027"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0027"
ms.assetid: 3a599876-9643-4c68-9457-3306858a73e9
caps.latest.revision: 12
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
# Compiler Error CS0027
Keyword 'this' is not available in the current context  
  
 The [this](../Topic/this%20\(C%23%20Reference\).md) keyword was found outside of a property, method, or constructor.  
  
 To fix this error, either modify the statement to eliminate use of the `this` keyword, and/or move part or all of the statement inside a property, method, or constructor.  
  
 The following example generates CS0027:  
  
```  
using System;  
using System.Collections.Generic;  
using System.Text;  
  
namespace ConsoleApplication3  
{  
    class MyClass  
    {  
  
        int err1 = this.Fun() + 1;  // CS0027   
  
        public int Fun()  
        {  
            return 10;  
        }  
  
        public void Test()  
        {  
            // valid use of this  
            int err = this.Fun() + 1;  
            Console.WriteLine(err);  
        }  
  
        public static void Main()  
        {  
            MyClass c = new MyClass();  
            c.Test();  
        }  
    }  
}  
```