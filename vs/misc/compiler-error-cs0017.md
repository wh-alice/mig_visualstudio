---
title: "Compiler Error CS0017 | Microsoft Docs"
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
  - "CS0017"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0017"
ms.assetid: 5e2a3eb3-6f6e-485d-8293-ceabea4d6905
caps.latest.revision: 10
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
# Compiler Error CS0017
Program 'output file name' has more than one entry point defined. Compile with /main to specify the type that contains the entry point.  
  
 A program can only have one [Main](/dotnet/csharp/programming-guide/main-and-command-args/main-and-command-line-arguments) method.  
  
 To resolve this error, you can either delete all Main methods in your code, except one, or you can use the [/main](/dotnet/csharp/language-reference/compiler-options/main-compiler-option) compiler option to specify which Main method you want to use.  
  
 The following sample generates CS0017:  
  
```  
// CS0017.cs  
// compile with: /target:exe  
public class clx  
{  
   static public void Main()  
   {  
   }  
}  
  
public class cly  
{  
   public static void Main()   // CS0017, delete one Main or use /main  
   {  
   }  
}  
```