---
title: "Compiler Error CS0653 | hehe"
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
  - "CS0653"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0653"
ms.assetid: c94043b9-b5d9-4294-921d-a4aead124d44
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
# Compiler Error CS0653
Cannot apply attribute class 'class' because it is abstract  
  
 An [abstract](../Topic/abstract%20\(C%23%20Reference\).md) custom attribute class cannot be used as an attribute.  
  
 The following sample generates CS0653:  
  
```  
// CS0653.cs  
using System;  
  
public abstract class MyAttribute : Attribute  
{  
}  
  
public class My2Attribute : MyAttribute  
{  
}  
  
[My]   // CS0653  
// try the following line instead  
// [My2]  
class MyClass  
{  
   public static void Main()  
   {  
   }  
}  
```