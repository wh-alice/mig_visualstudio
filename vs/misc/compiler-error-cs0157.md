---
title: "Compiler Error CS0157 | Microsoft Docs"
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
  - "CS0157"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0157"
ms.assetid: a5d9d506-81f8-47dd-85b6-85f8170bcbef
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
# Compiler Error CS0157
Control cannot leave the body of a finally clause  
  
 All of the statements in a [finally](/dotnet/csharp/language-reference/keywords/try-catch-finally) clause must execute. For more information, see [Exception Handling Statements](/dotnet/csharp/language-reference/keywords/exception-handling-statements) and [Exceptions and Exception Handling](/dotnet/csharp/programming-guide/exceptions/exceptions-and-exception-handling).  
  
 The following sample generates CS0157:  
  
```  
// CS0157.cs  
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
         }  
  
         finally  
         {  
            return;   // CS0157, cannot leave finally clause  
         }  
      }  
   }  
}  
```