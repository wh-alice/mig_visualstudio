---
title: "Compiler Error CS1040 | Microsoft Docs"
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
  - "CS1040"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1040"
ms.assetid: a988d665-ead5-489f-922d-ff2c4dd8a922
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
# Compiler Error CS1040
Preprocessor directives must appear as the first non-whitespace character on a line  
  
 A [preprocessor directive](/dotnet/csharp/language-reference/preprocessor-directives/index) was found on a line and was not the first token on the line. A directive must be the first token on the line.  
  
 The following sample generates CS1040:  
  
```  
// CS1040.cs  
/* Define a symbol, X */ #define X   // CS1040  
  
// try the following two lines instead  
// /* Define a symbol, X */  
// #define X  
  
public class MyClass  
{  
   public static void Main()  
   {  
   }  
}  
```