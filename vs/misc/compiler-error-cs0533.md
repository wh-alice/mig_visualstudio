---
title: "Compiler Error CS0533 | Microsoft Docs"
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
  - "CS0533"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0533"
ms.assetid: f8b38c5a-d365-4081-a101-6282bdd19069
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
# Compiler Error CS0533
'derived-class member' hides inherited abstract member 'base-class member'  
  
 A base [class](/dotnet/csharp/language-reference/keywords/class) method is hidden. Check the syntax of your declaration to see if it is correct.  
  
 For more information, see [base](/dotnet/csharp/language-reference/keywords/base).  
  
 The following sample generates CS0533:  
  
```  
// CS0533.cs  
namespace x  
{  
   abstract public class a  
   {  
      abstract public void f();  
   }  
  
   abstract public class b : a  
   {  
      new abstract public void f();   // CS0533  
      // try the following lines instead  
      // override public void f()  
      // {  
      // }  
  
      public static void Main()  
      {  
      }  
   }  
}  
```