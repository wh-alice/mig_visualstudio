---
title: "Compiler Error CS0182 | Microsoft Docs"
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
  - "CS0182"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0182"
ms.assetid: a9e97bb8-f06e-499f-aadf-26abc2082f98
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
# Compiler Error CS0182
An attribute argument must be a constant expression, typeof expression or array creation expression of an attribute parameter type  
  
 Certain restrictions apply to what kinds of arguments may be used with attributes. Note that in addition to the restrictions specified in the error message, the following types are NOT allowed as attribute arguments:  
  
-   [sbyte](/dotnet/csharp/language-reference/keywords/sbyte)  
  
-   [ushort](/dotnet/csharp/language-reference/keywords/ushort)  
  
-   [uint](/dotnet/csharp/language-reference/keywords/uint)  
  
-   [ulong](/dotnet/csharp/language-reference/keywords/ulong)  
  
-   [decimal](/dotnet/csharp/language-reference/keywords/decimal)  
  
 For more information, see [NOT IN BUILD: Global Attributes (C# Programming Guide)](http://msdn.microsoft.com/en-us/7c6c41f8-f0d5-4345-8987-3d91f9bae136).  
  
## Example  
 The following sample generates CS0182:  
  
```  
// CS0182.cs  
public class MyClass  
{  
    static string s = "Test";  
  
    [System.Diagnostics.ConditionalAttribute(s)]   // CS0182  
    // try the following line instead  
    // [System.Diagnostics.ConditionalAttribute("Test")]  
    void NonConstantArgumentToConditional()  
    {  
    }  
  
    public static void Main()  
    {  
    }  
}  
```