---
title: "Compiler Error CS1025"
ms.custom: ""
ms.date: "12/05/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS1025"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1025"
ms.assetid: 491c186f-cb40-47a9-9656-44fadfa18ae2
caps.latest.revision: 7
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
# Compiler Error CS1025
Single-line comment or end-of-line expected  
  
 A line with a [preprocessor directive](../Topic/C%23%20Preprocessor%20Directives.md) cannot have a multiline comment.  
  
 The following sample generates CS1025:  
  
```  
#if true /* hello  
*/   // CS1025  
#endif   // this is a good comment  
```  
  
 CS1025 could also occur if you attempt some invalid preprocessor directive, as follows:  
  
```  
// CS1025.cs  
#define a  
  
class Sample  
{  
   static void Main()  
   {  
      #if a 1   // CS1025, invalid syntax  
         System.Console.WriteLine("Hello, World!");  
      #endif  
   }  
}  
```