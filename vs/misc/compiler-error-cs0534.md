---
title: "Compiler Error CS0534"
ms.custom: ""
ms.date: "10/13/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0534"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0534"
ms.assetid: 39fde9d1-3041-41fc-9dc2-43394c13c6c9
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
# Compiler Error CS0534
'function1' does not implement inherited abstract member 'function2'  
  
 A class is required to implement all the [abstract](../Topic/abstract%20\(C%23%20Reference\).md) members in the base class, unless the class is also abstract.  
  
 The following sample generates CS0534:  
  
```  
// CS0534.cs  
namespace x  
{  
   abstract public class clx  
   {  
      public abstract void f();  
   }  
  
   public class cly : clx   // CS0534, no override for clx::f  
   {  
      // uncomment the following sample override to resolve CS0534  
      // override public void f()  
      // {  
      // }  
  
      public static int Main()  
      {  
         return 0;  
      }  
   }  
}  
```