---
title: "Compiler Error CS1028 | testtitle"
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
  - "CS1028"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1028"
ms.assetid: 9df07db3-256f-45e9-8323-26539c55a1d8
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
# Compiler Error CS1028
Unexpected preprocessor directive  
  
 A [preprocessor directive](../Topic/C%23%20Preprocessor%20Directives.md) was found but not expected.  
  
 For example, a `#endif` was found with no preceding `#if`.  
  
 The following sample generates CS1028:  
  
```  
// CS1028.cs  
#endif   // CS1028, no matching #if  
namespace x  
{  
   public class clx  
   {  
      public static void Main()  
      {  
      }  
   }  
}  
```