---
title: "Compiler Error CS0156 | Microsoft Docs"
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
  - "CS0156"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0156"
ms.assetid: 32026b1b-bcd7-4464-b63f-3b38c00452a6
caps.latest.revision: 9
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
# Compiler Error CS0156
A throw statement with no arguments is not allowed in a finally clause that is nested inside the nearest enclosing catch clause  
  
 A [throw](/dotnet/csharp/language-reference/keywords/throw) statement with no parameters can only appear in a **catch** clause that takes no parameters.  
  
 For more information, see [Exception Handling Statements](/dotnet/csharp/language-reference/keywords/exception-handling-statements) and [Exceptions and Exception Handling](/dotnet/csharp/programming-guide/exceptions/exceptions-and-exception-handling).  
  
 The following sample generates CS0156:  
  
```  
// CS0156.cs  
using System;  
  
namespace MyNamespace  
{  
   public class MyClass2 : Exception  
   {  
   }  
  
   public class MyClass  
   {  
      public static void Main()  
      {  
         try  
         {  
            throw;   // CS0156  
         }  
  
         catch(MyClass2)  
         {  
            throw;   // this throw is valid  
         }  
      }  
   }  
}  
```