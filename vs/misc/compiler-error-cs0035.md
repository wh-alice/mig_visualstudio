---
title: "Compiler Error CS0035 | testtitle"
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
  - "CS0035"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0035"
ms.assetid: a622113e-98a4-4583-992c-1fb55139320a
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
# Compiler Error CS0035
Operator 'operator' is ambiguous on an operand of type 'type'  
  
 The compiler has more than one available conversion and does not know which to choose before applying the operator. For more information, see [Templated User Defined Conversions](../misc/templated-user-defined-conversions.md) and [Conversion Operators](../Topic/Conversion%20Operators%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0035:  
  
```  
// CS0035.cs  
class MyClass  
{  
   private int i;  
  
   public MyClass(int i)  
   {  
      this.i = i;  
   }  
  
   public static implicit operator double(MyClass x)  
   {  
      return (double) x.i;  
   }  
  
   public static implicit operator decimal(MyClass x)  
   {  
      return (decimal) x.i;  
   }  
}  
  
class MyClass2  
{  
   static void Main()  
   {  
      MyClass x = new MyClass(7);  
      object o = - x;   // CS0035  
      // try a cast:  
      // object o = - (double)x;  
   }  
}  
  
```