---
title: "Compiler Error CS0180 | Microsoft Docs"
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
  - "CS0180"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0180"
ms.assetid: a21bf0a2-ed5a-4ddd-88d3-240babc5888a
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
# Compiler Error CS0180
'member' cannot be both extern and abstract  
  
 The [abstract](/dotnet/csharp/language-reference/keywords/abstract) and [extern](/dotnet/csharp/language-reference/keywords/extern) keywords are mutually exclusive. The `extern` keyword means that the member is defined outside the file, and **abstract** means that the implementation is provided in a derived class. For more information, see [Methods](/dotnet/csharp/programming-guide/classes-and-structs/methods).  
  
 The following sample generates CS0180:  
  
```  
// CS0180.cs  
namespace MyNamespace  
{  
   public class MyClass  
   {  
      public extern abstract int Foo(int a);   // CS0180  
  
      public static void Main()  
      {  
      }  
   }  
}  
```