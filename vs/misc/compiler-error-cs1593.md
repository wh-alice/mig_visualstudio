---
title: "Compiler Error CS1593"
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
  - "CS1593"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1593"
ms.assetid: 7476e799-8a8d-457d-b4e7-2d5e073799d8
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
# Compiler Error CS1593
Delegate 'del' does not take 'number' arguments  
  
 The number of arguments passed to a [delegate](../Topic/delegate%20\(C%23%20Reference\).md) invocation does not agree with the number of parameters in the delegate declaration.  
  
 The following sample generates CS1593:  
  
```  
// CS1593.cs  
using System;  
delegate string func(int i);   // declare delegate  
  
class a  
{  
   public static void Main()  
   {  
      func dt = new func(z);  
      x(dt);  
   }  
  
   public static string z(int j)  
   {  
      Console.WriteLine(j);  
      return j.ToString();  
   }  
  
   public static void x(func hello)  
   {  
      hello(8, 9);   // CS1593  
      // try the following line instead  
      // hello(8);  
   }  
}  
```