---
title: "Compiler Error CS0549 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0549"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0549"
ms.assetid: ae965019-9dee-4f28-9e9a-6f379bd0d757
caps.latest.revision: 8
author: "BillWagner"
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
# Compiler Error CS0549
'function' is a new virtual member in sealed class 'class'  
  
 A [sealed](/dotnet/csharp/language-reference/keywords/sealed)[class](/dotnet/csharp/language-reference/keywords/class) cannot be used as a base class.  Therefore, it is useless to have a virtual method in sealed class.  
  
 The following sample generates CS0549:  
  
```  
// CS0549.cs  
// compile with: /target:library  
sealed public class MyClass  
{  
   virtual public void TestMethod() {}   // CS0549  
   public void TestMethod2() {}   // OK  
}  
```