---
title: "Compiler Error CS0431"
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
  - "CS0431"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0431"
ms.assetid: 05da7ea7-f33d-48d4-948e-d64be56f91ba
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
# Compiler Error CS0431
Cannot use alias 'identifier' with '::' since the alias references a type. Use '.' instead.  
  
 You used "::" with an alias that references a type. To resolve this error, use the "." operator.  
  
 The following sample generates CS0431:  
  
```  
// CS0431.cs  
using A = Outer;  
  
public class Outer   
{  
   public class Inner   
   {  
      public static void Meth() {}  
   }  
}  
  
public class MyClass  
{  
   public static void Main()  
   {  
      A::Inner.Meth();   // CS0431  
      A.Inner.Meth();   // OK  
   }  
}  
```