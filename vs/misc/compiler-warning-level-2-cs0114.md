---
title: "Compiler Warning (level 2) CS0114 | Microsoft Docs"
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
  - "CS0114"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0114"
ms.assetid: 9647772b-d581-4620-981e-f9c607d4a1af
caps.latest.revision: 7
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
# Compiler Warning (level 2) CS0114
'function1' hides inherited member 'function2'. To make the current method override that implementation, add the override keyword. Otherwise add the new keyword.  
  
 A declaration in a class conflicts with a declaration in a base class such that the base class member will be hidden.  
  
 For more information, see [base](/dotnet/csharp/language-reference/keywords/base).  
  
 The following sample generates CS0114:  
  
```  
// CS0114.cs  
// compile with: /W:2 /warnaserror  
abstract public class clx  
{  
   public abstract void f();  
}  
  
public class cly : clx  
{  
   public void f() // CS0114, hides base class member  
   // try the following line instead  
   // override public void f()  
   {  
   }  
  
   public static void Main()  
   {  
   }  
}  
```