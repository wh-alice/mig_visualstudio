---
title: "Compiler Error CS0079 | Microsoft Docs"
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
  - "CS0079"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0079"
ms.assetid: 71c85883-b72f-402f-a828-18ca92976273
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
# Compiler Error CS0079
The event 'event' can only appear on the left hand side of += or -=  
  
 An [event](/dotnet/csharp/language-reference/keywords/event) was called incorrectly. For more information, see [Events](/dotnet/csharp/programming-guide/events/index) and [Delegates](/dotnet/csharp/programming-guide/delegates/index).  
  
 The following sample generates CS0079:  
  
```  
// CS0079.cs  
using System;  
  
public delegate void MyEventHandler();  
  
public class Class1  
{  
   private MyEventHandler _e;  
  
   public event MyEventHandler Pow  
   {  
      add  
      {  
         _e += value;  
         Console.WriteLine("in add accessor");  
      }  
      remove  
      {  
         _e -= value;  
         Console.WriteLine("in remove accessor");  
      }  
   }  
  
   public void Handler()  
   {  
   }  
  
   public void Fire()  
   {  
      if (_e != null)  
      {  
         Pow();   // CS0079  
         // try the following line instead  
         // _e();  
      }  
   }  
  
   public static void Main()  
   {  
      Class1 p = new Class1();  
      p.Pow += new MyEventHandler(p.Handler);  
      p._e();  
      p.Pow += new MyEventHandler(p.Handler);  
      p._e();  
      p._e -= new MyEventHandler(p.Handler);  
      if (p._e != null)  
      {  
         p._e();  
      }  
      p.Pow -= new MyEventHandler(p.Handler);  
      if (p._e != null)  
      {  
         p._e();  
      }  
   }  
}  
```