---
title: "Compiler Error CS0209 | Microsoft Docs"
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
  - "CS0209"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0209"
ms.assetid: a408a869-02db-414f-97c1-bfb1637f6155
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
# Compiler Error CS0209
The type of local declared in a fixed statement must be a pointer type  
  
 The variable that you declare in a [fixed statement](/dotnet/csharp/language-reference/keywords/fixed-statement) must be a pointer. For more information, see [Unsafe Code and Pointers](/dotnet/csharp/programming-guide/unsafe-code-pointers/index).  
  
 The following sample generates CS0209:  
  
```  
// CS0209.cs  
// compile with: /unsafe  
  
class Point  
{  
   public int x, y;  
}  
  
public class MyClass  
{  
   unsafe public static void Main()  
   {  
      Point pt = new Point();  
  
      fixed (int i)    // CS0209  
      {  
      }  
      // try the following lines instead  
      /*  
      fixed (int* p = &pt.x)  
      {  
      }  
      fixed (int* q = &pt.y)  
      {  
      }  
      */  
   }  
}  
```