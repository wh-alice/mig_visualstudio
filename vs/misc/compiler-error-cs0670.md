---
title: "Compiler Error CS0670"
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
  - "CS0670"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0670"
ms.assetid: 59379171-284f-4d55-8741-af6a97879abc
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
# Compiler Error CS0670
Field cannot have void type  
  
 A field was declared to be of type [void](../Topic/void%20\(C%23%20Reference\).md).  
  
 The following sample generates CS0670:  
  
```  
// CS0670.cs  
class C  
{  
   void f;   // CS0670  
   // try the following line instead  
   // public int f;  
  
   public static void Main()  
   {  
      C myc = new C();  
      myc.f = 0;  
   }  
}  
```