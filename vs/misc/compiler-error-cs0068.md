---
title: "Compiler Error CS0068"
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
  - "CS0068"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0068"
ms.assetid: 9c9ac915-e12f-4ceb-8eb0-806790f11a09
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
# Compiler Error CS0068
'event': event in interface cannot have initializer  
  
 An event in an interface cannot have an initializer. For more information, see [Interfaces](../Topic/Interfaces%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0068:  
  
```  
// CS0068.cs  
  
delegate void MyDelegate();  
  
interface I  
{  
   event MyDelegate d = new MyDelegate(M.f);   // CS0068  
   // try the following line instead  
   // event MyDelegate d2;  
}  
  
class M  
{  
   event MyDelegate d = new MyDelegate(M.f);  
  
   public static void f()  
   {  
   }  
  
   public static void Main()  
   {  
   }  
}  
```