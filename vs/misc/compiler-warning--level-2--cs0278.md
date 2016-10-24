---
title: "Compiler Warning (level 2) CS0278"
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
  - "CS0278"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0278"
ms.assetid: 5418cbbe-bcec-4379-a6f6-410987beb96a
caps.latest.revision: 10
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
# Compiler Warning (level 2) CS0278
'type' does not implement the 'pattern name' pattern. 'method name' is ambiguous with 'method name'.  
  
 There are several statements in C# that rely on defined patterns, such as `foreach` and `using`. For example, `foreach` relies on the collection class implementing the "enumerable" pattern.  
  
 CS0278 can occur if the compiler is unable to make the match due to ambiguities. For example, the "enumerable" pattern requires that there be a method called `MoveNext`, and your code might contain two methods called `MoveNext`. The compiler will attempt to find an interface to use, but it is recommended that you determine and resolve the cause of the ambiguity.  
  
 For more information, see [How to: Access a Collection Class with foreach](../Topic/How%20to:%20Access%20a%20Collection%20Class%20with%20foreach%20\(C%23%20Programming%20Guide\).md).  
  
## Example  
 The following sample generates CS0278.  
  
```  
// CS0278.cs  
using System.Collections.Generic;  
public class myTest   
{  
   public static void TestForeach<W>(W w)   
      where W: IEnumerable<int>, IEnumerable<string>  
   {  
      foreach (int i in w) {}   // CS0278  
   }  
}  
```