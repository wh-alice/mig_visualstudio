---
title: "Compiler Error CS0139"
ms.custom: ""
ms.date: "10/25/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0139"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0139"
ms.assetid: 235ba3d4-566c-4ef6-801a-a338f4f2a12d
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
# Compiler Error CS0139
No enclosing loop out of which to break or continue  
  
 A break or continue statement was encountered outside of a loop.  
  
 For more information, see [Jump Statements](../Topic/Jump%20Statements%20\(C%23%20Reference\).md).  
  
 The following sample generates CS0139 twice:  
  
```  
// CS0139.cs  
namespace x  
{  
   public class a  
   {  
      public static void Main()  
      {  
         continue;  // CS0139  
         break;     // CS0139  
      }  
   }  
}  
```