---
title: "Compiler Error CS0191 | Microsoft Docs"
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
  - "CS0191"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0191"
ms.assetid: 512479e4-656e-4dcb-8d71-801541d72dcd
caps.latest.revision: 10
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
# Compiler Error CS0191
Property or indexer 'name' cannot be assigned to -- it is read only  
  
 A [readonly](/dotnet/csharp/language-reference/keywords/readonly) field can only take an assignment in a constructor or at declaration. For more information, see [Constructors](/dotnet/csharp/programming-guide/classes-and-structs/constructors).  
  
 CS0191 also results if the `readonly` field is [static](/dotnet/csharp/language-reference/keywords/static) and the constructor is not marked `static`.  
  
## Example  
 The following sample generates CS0191.  
  
```  
// CS0191.cs  
class MyClass  
{  
    public readonly int TestInt = 6;  // OK to assign to readonly field in declaration  
  
    MyClass()  
    {  
        TestInt = 11; // OK to assign to readonly field in constructor  
    }  
  
    public void TestReadOnly()  
    {  
        TestInt = 19;                  // CS0191  
    }  
  
    public static void Main()  
    {  
    }  
}  
```