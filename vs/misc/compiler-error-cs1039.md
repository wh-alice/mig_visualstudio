---
title: "Compiler Error CS1039"
ms.custom: na
ms.date: "10/01/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "CS1039"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1039"
ms.assetid: 266e9f7f-fe17-445a-aefd-6b7795167d68
caps.latest.revision: 8
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
# Compiler Error CS1039
Unterminated string literal  
  
 The compiler detected an ill-formed [string](../Topic/string%20\(C%23%20Reference\).md) literal.  
  
## Example  
 The following sample generates CS1039. To resolve the error, add the terminating quotation mark.  
  
```  
// CS1039.cs  
public class MyClass  
{  
    public static void Main()  
    {  
        string b = @"hello, world;   // CS1039  
    }  
}  
```