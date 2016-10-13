---
title: "Compiler Error CS0215"
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
  - "CS0215"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0215"
ms.assetid: 2060440d-be22-4c10-8b26-43b08b615447
caps.latest.revision: 8
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
# Compiler Error CS0215
The return type of operator True or False must be bool  
  
 User-defined [true](../Topic/true%20\(C%23%20Reference\).md) and [false](../Topic/false%20\(C%23%20Reference\).md) operators must have a return type of [bool](../Topic/bool%20\(C%23%20Reference\).md). For more information, see [Overloadable Operators](../Topic/Overloadable%20Operators%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0215:  
  
```  
// CS0215.cs  
class MyClass  
{  
   public static int operator true (MyClass MyInt)   // CS0215  
   // try the following line instead  
   // public static bool operator true (MyClass MyInt)  
   {  
      return true;  
   }  
  
   public static int operator false (MyClass MyInt)   // CS0215  
   // try the following line instead  
   // public static bool operator false (MyClass MyInt)  
   {  
      return true;  
   }  
  
   public static void Main()  
   {  
   }  
}  
```