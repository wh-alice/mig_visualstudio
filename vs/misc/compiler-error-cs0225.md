---
title: "Compiler Error CS0225 | Microsoft Docs"
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
  - "CS0225"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0225"
ms.assetid: 0b0cd72b-c47a-44d1-9b27-d1a1fad06807
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
# Compiler Error CS0225
The params parameter must be a single dimensional array  
  
 When using the [params](/dotnet/csharp/language-reference/keywords/params) keyword, you must specify a single-dimensional array of the data type. For more information, see [Methods](/dotnet/csharp/programming-guide/classes-and-structs/methods).  
  
## Example  
 The following sample generates CS0225:  
  
```  
// CS0225.cs  
public class MyClass  
{  
    public static void TestParams(params int a)   // CS0225  
    // try the following line instead  
    // public static void TestParams(params int[] a)  
    {  
    }  
  
    public static void Main()  
    {  
        TestParams(1);  
    }  
}  
```