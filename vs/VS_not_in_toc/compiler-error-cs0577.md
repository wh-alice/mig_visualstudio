---
title: "Compiler Error CS0577"
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
  - "CS0577"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0577"
ms.assetid: 34f8f453-f016-4f2c-981a-0d61449cd74b
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
# Compiler Error CS0577
The Conditional attribute is not valid on 'function' because it is a constructor, destructor, operator, or explicit interface implementation  
  
 `Conditional` cannot be applied to the specified methods.  
  
 For example, you cannot use some attributes on an explicit interface definition. The following sample generates CS0577:  
  
```  
// CS0577.cs  
// compile with: /target:library  
interface I  
{  
   void m();  
}  
  
public class MyClass : I  
{  
   [System.Diagnostics.Conditional("a")]   // CS0577  
   void I.m() {}  
}  
```