---
title: "Compiler Error CS0438"
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
  - "CS0438"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0438"
ms.assetid: 92c91ecb-8d6a-4850-84eb-c095c3c957f1
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
# Compiler Error CS0438
The type 'type' in 'module_1' conflicts with the namespace 'namespace' in 'module_2'.  
  
 This error occurs when a type in a source file conflicts with a namespace in another source file. This typically happens when one or both come from an added module. To resolve, rename the type or the namespace that caused the conflict.  
  
 The following example generates CS0438:  
  
 Compile this file first:  
  
```  
// CS0438_1.cs  
// compile with: /target:module  
public class Util  
{  
   public class A { }  
}  
```  
  
 Then compile this file:  
  
```  
// CS0438_2.cs  
// compile with: /target:module  
namespace Util   
{  
   public class A { }  
}  
```  
  
 And then compile this file:  
  
```  
// CS0438_3.cs  
// compile with: /addmodule:CS0438_1.netmodule /addmodule:CS0438_2.netmodule  
using System;  
public class Test  
{  
   public static void Main() {  
      Console.WriteLine(typeof(Util.A));   // CS0438  
   }  
}  
  
```