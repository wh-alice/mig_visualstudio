---
title: "Compiler Error CS0213 | Microsoft Docs"
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
  - "CS0213"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0213"
ms.assetid: 3c1d55e3-2b84-4c28-8206-ef65869a898c
caps.latest.revision: 11
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
# Compiler Error CS0213
You cannot use the fixed statement to take the address of an already fixed expression  
  
 A local variable in an [unsafe](../Topic/unsafe%20\(C%23%20Reference\).md) method or a parameter is already fixed (on the stack), so you cannot take the address of either of these two variables in a [fixed](../Topic/fixed%20Statement%20\(C%23%20Reference\).md) expression. For more information, see [Unsafe Code and Pointers](../Topic/Unsafe%20Code%20and%20Pointers%20\(C%23%20Programming%20Guide\).md).  
  
## Example  
 The following sample generates CS0213.  
  
```  
// CS0213.cs  
// compile with: /unsafe  
public class MyClass  
{  
   unsafe public static void Main()  
   {  
      int i = 45;  
      fixed (int *j = &i) { }  // CS0213  
      // try the following line instead  
      // int* j = &i;  
  
      int[] a = new int[] {1,2,3};  
      fixed (int *b = a)  
      {  
         fixed (int *c = b) { }  // CS0213  
         // try the following line instead  
         // int *c = b;  
      }  
   }  
}  
```