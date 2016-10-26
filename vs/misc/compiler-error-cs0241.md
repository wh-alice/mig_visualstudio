---
title: "Compiler Error CS0241"
ms.custom: ""
ms.date: "10/25/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0241"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "default method parameter values"
  - "defaults, parameter values"
  - "defaults, method parameter values"
  - "default parameter values"
  - "CS0241"
ms.assetid: be31b194-3de5-4aab-b23a-6cf790f940ab
caps.latest.revision: 10
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
# Compiler Error CS0241
Default parameter specifiers are not permitted  
  
 [Method parameters](../Topic/Method%20Parameters%20\(C%23%20Reference\).md) cannot have default values. Use method overloads if you want to achieve the same effect. For more information, see [Passing Parameters](../Topic/Passing%20Parameters%20\(C%23%20Programming%20Guide\).md).  
  
## Example  
 The following sample generates CS0241. In addition, the sample shows how to simulate, with overloading, a method with default arguments.  
  
```  
// CS0241.cs  
public class A  
{  
   public void Test(int i = 9) {}   // CS0241  
}  
  
public class B  
{  
   public void Test() { Test(9); }  
   public void Test(int i)  {}  
}  
  
public class C  
{  
   public static void Main()  
   {   
      B x = new B();  
      x.Test();  
   }  
}  
```