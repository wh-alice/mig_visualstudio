---
title: "Compiler Error CS0192 | Microsoft Docs"
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
  - "CS0192"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0192"
ms.assetid: d3fb6d18-dbf3-42c3-a280-afe55b97c2d1
caps.latest.revision: 11
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
# Compiler Error CS0192
Fields of static readonly field 'name' cannot be passed ref or out (except in a static constructor)  
  
 A field (variable) marked with the [readonly](/dotnet/csharp/language-reference/keywords/readonly) keyword cannot be passed either to a [ref](/dotnet/csharp/language-reference/keywords/ref) or [out](/dotnet/csharp/language-reference/keywords/out) parameter except inside a constructor. For more information, see [Fields](/dotnet/csharp/programming-guide/classes-and-structs/fields).  
  
 CS0192 also results if the `readonly` field is [static](/dotnet/csharp/language-reference/keywords/static) and the constructor is not marked `static`.  
  
## Example  
 The following sample generates CS0192.  
  
```  
// CS0192.cs  
class MyClass  
{  
    public readonly int TestInt = 6;  
    static void TestMethod(ref int testInt)  
    {  
        testInt = 0;  
    }  
  
    MyClass()  
    {  
        TestMethod(ref TestInt);   // OK  
    }  
  
    public void PassReadOnlyRef()  
    {  
        TestMethod(ref TestInt);   // CS0192  
    }  
  
    public static void Main()  
    {  
    }  
}  
```