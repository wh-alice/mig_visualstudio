---
title: "Compiler Error CS1611 | Microsoft Docs"
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
  - "CS1611"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1611"
ms.assetid: 48bfba77-6be2-4242-b1d2-98bf471b6d1e
caps.latest.revision: 7
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
# Compiler Error CS1611
The params parameter cannot be declared as ref or out  
  
 The keywords [ref](/dotnet/csharp/language-reference/keywords/ref) or [out](/dotnet/csharp/language-reference/keywords/out) cannot be used with the [params](/dotnet/csharp/language-reference/keywords/params) keyword.  
  
 The following sample generates CS1611:  
  
```  
// CS1611.cs  
public class MyClass  
{  
   public static void Test(params ref int[] a)   // CS1611, remove ref  
   {  
   }  
  
   public static void Main()  
   {  
      Test(1);  
   }  
}  
```