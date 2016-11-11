---
title: "Compiler Error CS0447 | Microsoft Docs"
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
  - "CS0447"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0447"
ms.assetid: a25486c5-e9bf-4528-8533-c1aaab22ace0
caps.latest.revision: 13
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
# Compiler Error CS0447
Attributes cannot be used on type arguments, only on type parameters  
  
 This error occurs when you apply an attribute to a type argument that occurs in an invocation statement. It is acceptable to apply an attribute to a type parameter in a class or method declaration statement such as the following:  
  
```  
class C<[some attribute] T> {…}  
```  
  
 The following line of code will generate this error. It is assumed that the class `C`, defined in the previous line of code, has a static method called `MyStaticMethod`.  
  
```  
C<[some attribute] T>.MyStaticMethod();  
```  
  
## Example  
 The following code generates error CS0447.  
  
```  
// CS0447.cs  
using System;  
namespace Test41  
{  
    public interface I<A>   
    {  
        void Meth<B>();  
    }  
    public class B : I<int>   
    {  
        void I<[Test] int>.Meth<X>() { }  // CS0447  
    }  
}  
```