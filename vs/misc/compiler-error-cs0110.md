---
title: "Compiler Error CS0110"
ms.custom: ""
ms.date: "10/13/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0110"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0110"
ms.assetid: 0bfe7071-1194-4142-a1a1-6190ee92b1d4
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
# Compiler Error CS0110
The evaluation of the constant value for 'const declaration' involves a circular definition  
  
 The declaration of a [const](../Topic/const%20\(C%23%20Reference\).md) variable (`a`) cannot reference another const variable (`b`) that also references (`a`).  
  
 The following sample generates CS0110:  
  
```  
// CS0110.cs  
namespace MyNamespace  
{  
   public class A  
   {  
      public static void Main()  
      {  
      }  
   }  
  
   public class B : A  
   {  
      public const int i = c + 1;   // CS0110, c already references i  
      public const int c = i + 1;  
      // the following line would be OK  
      // public const int c = 10;  
   }  
}  
```  
  
## See Also  
 [Constants](../Topic/Constants%20\(C%23%20Programming%20Guide\).md)