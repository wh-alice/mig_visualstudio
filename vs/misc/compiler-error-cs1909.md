---
title: "Compiler Error CS1909"
ms.custom: na
ms.date: "10/13/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "CS1909"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1909"
ms.assetid: d465a107-0911-4440-8b3a-1e5dea6fda3c
caps.latest.revision: 9
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
# Compiler Error CS1909
The DefaultValue attribute is not applicable on parameters of type 'type'  
  
 CS1909 is generated when you use a `DefaultValue` attribute that is not applicable on the parameter type.  
  
## Example  
 The following sample generates CS1909.  
  
```  
// CS1909.cs  
// compile with: /target:library  
using System.Runtime.InteropServices;  
  
public interface ISomeInterface  
{  
   void Test1([DefaultParameterValue(new int[] {1, 2})] int[] arr1);   // CS1909  
  
   void Test2([DefaultParameterValue("Test String")] string s);   // OK  
}  
```