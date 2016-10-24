---
title: "Compiler Error CS1020 | testtitle"
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
  - "CS1020"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1020"
ms.assetid: e8860769-a847-4248-a37b-77a59863467c
caps.latest.revision: 7
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
# Compiler Error CS1020
Overloadable binary operator expected  
  
 An attempt was made to define an [operator overload](../Topic/Overloadable%20Operators%20\(C%23%20Programming%20Guide\).md), but the operator was not a binary operator, which takes two parameters.  
  
 The following sample generates CS1020:  
  
```  
// CS1020.cs  
public class iii  
{  
   public static int operator ++(iii aa, int bb)   // CS1020, change ++ to +  
   {  
      return 0;  
   }  
  
   public static void Main()  
   {  
   }  
}  
```