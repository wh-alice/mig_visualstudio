---
title: "Compiler Error CS0553"
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
  - "CS0553"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0553"
ms.assetid: d2d6ddb1-9294-4e85-83d8-c35bd7a70f5b
caps.latest.revision: 6
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
# Compiler Error CS0553
'conversion routine' : user defined conversion to/from base class  
  
 User-defined conversions to values of a base class are not allowed; you do not need such an operator.  
  
 The following sample generates CS0553:  
  
```  
// CS0553.cs  
namespace x  
{  
   public class ii  
   {  
   }  
  
   public class a : ii  
   {  
      // delete the conversion routine to resolve CS0553  
      public static implicit operator ii(a aa) // CS0553  
      {  
         return new ii();  
      }  
  
      public static void Main()  
      {  
      }  
   }  
}  
```