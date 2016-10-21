---
title: "Compiler Error CS0245 | hehe"
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
  - "CS0245"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0245"
ms.assetid: 3f2beb2f-a510-4568-9d11-bb1f65066acd
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
# Compiler Error CS0245
Destructors and object.Finalize cannot be called directly. Consider calling IDisposable.Dispose if available.  
  
 For more information, see [Programming Essentials for Garbage Collection](../Topic/Garbage%20Collection.md) and [Destructors](../Topic/Destructors%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0245:  
  
```  
// CS0245.cs  
using System;  
using System.Collections;  
  
class MyClass // : IDisposable  
{  
   /*  
   public void Dispose()  
   {  
      // cleanup code goes here  
   }  
   */  
  
   void m()  
   {  
      this.Finalize();   // CS0245  
      // this.Dispose();  
   }  
  
   public static void Main()  
   {  
   }  
}  
```