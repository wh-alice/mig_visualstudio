---
title: "Compiler Error CS0205 | Microsoft Docs"
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
  - "CS0205"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0205"
ms.assetid: 616d98cf-e7a5-4f8e-93da-fcd6e1e4de35
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
# Compiler Error CS0205
Cannot call an abstract base member: 'method'  
  
 You cannot call an [abstract](/dotnet/csharp/language-reference/keywords/abstract) method because it does not have a method body. For more information, see [Abstract and Sealed Classes and Class Members](/dotnet/csharp/programming-guide/classes-and-structs/abstract-and-sealed-classes-and-class-members).  
  
 The following sample generates CS0205:  
  
```  
// CS0205.cs  
abstract public class MyClass  
{  
   abstract public void M();  
}  
  
public class MyClass2 : MyClass  
{  
   public override void M()  
   {  
      base.M();   // CS0205, delete this line  
   }  
  
   public static void Main()  
   {  
   }  
}  
```