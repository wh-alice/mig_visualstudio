---
title: "Compiler Error CS0175 | Microsoft Docs"
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
  - "CS0175"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0175"
ms.assetid: cedd769d-8258-4235-a321-362981b9f84b
caps.latest.revision: 12
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
# Compiler Error CS0175
Use of keyword 'base' is not valid in this context  
  
 The [base](/dotnet/csharp/language-reference/keywords/base) keyword must be used to specify a particular member of the base class. For more information, see [Constructors](/dotnet/csharp/programming-guide/classes-and-structs/constructors).  
  
 The following sample generates CS0175:  
  
```  
// CS0175.cs  
using System;  
class BaseClass  
{  
    public int TestInt = 0;  
}  
  
class MyClass : BaseClass  
{  
    public static void Main()  
    {  
        MyClass aClass = new MyClass();  
        aClass.BaseTest();  
    }  
  
    public void BaseTest()  
    {  
        Console.WriteLine(base); // CS0175  
        // Try the following line instead:  
        // Console.WriteLine(base.TestInt);  
        base = 9;   // CS0175  
  
        // Try the following line instead:  
        // base.TestInt = 9;  
    }  
}  
```