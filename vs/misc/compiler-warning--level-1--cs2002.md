---
title: "Compiler Warning (level 1) CS2002 | testtitle"
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
  - "CS2002"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS2002"
ms.assetid: 4acd054e-d3fe-4be6-a660-53a0a5e8c6a4
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
# Compiler Warning (level 1) CS2002
Source file 'file' specified multiple times  
  
 A source file name was passed to the compiler more than once. You can only specify a file once to the compiler to build an output file.  
  
 This warning cannot be suppressed by the [/nowarn](../Topic/-nowarn%20\(C%23%20Compiler%20Options\).md) option.  
  
 The following sample generates CS2002:  
  
```  
// CS2002.cs  
// compile with: CS2002.cs  
public class A  
{  
public static void Main(){}  
}  
```  
  
 To generate the error, compile the example with the command line:  
  
```  
csc CS2002.cs CS2002.cs  
```