---
title: "Compiler Error CS0080 | Microsoft Docs"
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
  - "CS0080"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0080"
ms.assetid: 99035371-37d1-48b2-a8b9-e8a1ebd04f0f
caps.latest.revision: 8
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
# Compiler Error CS0080
Constraints are not allowed on non-generic declarations  
  
 The syntax found may only be used in a generic declaration to apply constraints to the type parameter. For more information, see [Generics](../Topic/Generics%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0080 because MyClass is not a generic class and Foo is not a generic method.  
  
```  
namespace MyNamespace  
{  
    public class MyClass where MyClass : System.IDisposable // CS0080    //the following line shows an example of correct syntax  
    //public class MyClass<T> where T : System.IDisposable  
    {  
        public void Foo() where Foo : new() // CS0080  
        //the following line shows an example of correct syntax  
        //public void Foo<U>() where U : struct  
        {  
        }  
    }  
  
    public class Program  
    {  
        public static void Main()  
        {  
        }  
    }  
}  
```