---
title: "Compiler Warning (level 2) CS0435"
ms.custom: na
ms.date: "10/01/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "CS0435"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0435"
ms.assetid: e70cd8c1-d399-4af8-8b1e-69a1de389aad
caps.latest.revision: 7
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
# Compiler Warning (level 2) CS0435
The namespace 'namespace' in 'assembly' conflicts with the imported type 'type' in 'assembly'. Using the namespace defined in 'assembly'..  
  
 This warning is issued when a namespace in a source file (file_2) conflicts with an imported type in file_1. The compiler uses the one in the source file.  
  
 The following example generates CS0435:  
  
 Compile this file first:  
  
```  
// CS0435_1.cs  
// compile with: /t:library  
public class Util   
{  
   public class A { }  
}  
```  
  
 Then, compile this file:  
  
```  
// CS0435_2.cs  
// compile with: /r:CS0435_1.dll  
  
using System;  
  
namespace Util   
{  
   public class A { }  
}  
  
public class Test   
{  
   public static void Main()   
   {  
      Console.WriteLine(typeof(Util.A)); // CS0435  
   }  
}  
```