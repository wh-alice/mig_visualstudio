---
title: "Compiler Error CS1515 | hehe"
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
  - "CS1515"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1515"
ms.assetid: 17d9dbbe-14a0-4c80-a942-82fa6ec2b0b0
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
# Compiler Error CS1515
'in' expected  
  
 In a [foreach, in](../Topic/foreach,%20in%20\(C%23%20Reference\).md) statement, the "in" part is missing.  
  
## Example  
 The following sample generates CS1515:  
  
```  
using System;  
  
class Driver  
{  
   static void Main()  
   {  
      int[] arr = new int[] {1, 2, 3};  
  
      // try the following line instead  
      // foreach (int x in arr)  
      foreach (int x arr)      // CS1515, "in" is missing  
      {  
         Console.WriteLine(x);  
      }  
   }  
}  
```