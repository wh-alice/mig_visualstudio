---
title: "Compiler Error CS0674 | Microsoft Docs"
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
  - "CS0674"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0674"
ms.assetid: 9ebfac30-6de8-4503-b4f0-d79f7398e3d5
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
# Compiler Error CS0674
Do not use 'System.ParamArrayAttribute'. Use the 'params' keyword instead.  
  
 The C# compiler does not allow for the use of <xref:System.ParamArrayAttribute?displayProperty=fullName>; use [params](/dotnet/csharp/language-reference/keywords/params) instead.  
  
 The following sample generates CS0674:  
  
```  
// CS0674.cs  
using System;  
public class MyClass   
{  
  
   public static void UseParams([ParamArray] int[] list)   // CS0674  
   // try the following line instead  
   // public static void UseParams(params int[] list)   
   {  
      for ( int i = 0 ; i < list.Length ; i++ )  
         Console.WriteLine(list[i]);  
      Console.WriteLine();  
   }  
  
   public static void Main()   
   {  
      UseParams(1, 2, 3);  
   }  
}  
```