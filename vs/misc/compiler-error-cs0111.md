---
title: "Compiler Error CS0111"
ms.custom: na
ms.date: "10/02/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "CS0111"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0111"
ms.assetid: 87afb689-f27b-451d-84eb-d6bdf17aea41
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
# Compiler Error CS0111
Type 'class' already defines a member called 'member' with the same parameter types  
  
 CS0111 occurs if a class contains two member declarations with the same name and parameter types. For more information, see [Methods](../Topic/Methods%20\(C%23%20Programming%20Guide\).md).  
  
## Example  
 The following sample generates CS0111.  
  
```  
// CS0111.cs  
class A  
{  
   void Test() { }  
   public static void Test(){}   // CS0111  
  
   public static void Main() {}  
}  
```