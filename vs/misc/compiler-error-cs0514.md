---
title: "Compiler Error CS0514 | Microsoft Docs"
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
  - "CS0514"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0514"
ms.assetid: 74ce3010-f9e9-458c-8b68-cfb908a3e7a2
caps.latest.revision: 10
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
# Compiler Error CS0514
'constructor' : static constructor cannot have an explicit 'this' or 'base' constructor call  
  
 Calling `this` in the static constructor is not allowed because the static constructor is called automatically before creating any instance of the class. Also, static constructors are not inherited, and cannot be called directly.  
  
 For more information, see [this](/dotnet/csharp/language-reference/keywords/this) and [base](/dotnet/csharp/language-reference/keywords/base).  
  
## Example  
 The following example generates CS0514:  
  
```  
// CS0514.cs  
class A  
{  
    static A() : base(0) // CS0514  
    {  
    }  
  
    public A(object o)  
    {  
    }  
}  
  
class B  
{  
    static B() : this(null) // CS0514  
    {  
    }  
  
    public B(object o)  
    {  
    }  
}  
```