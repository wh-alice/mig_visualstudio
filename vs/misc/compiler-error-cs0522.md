---
title: "Compiler Error CS0522"
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
  - "CS0522"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0522"
ms.assetid: f749f21e-92ee-495c-9b53-179ce9342d05
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
# Compiler Error CS0522
'constructor' : structs cannot call base class constructors  
  
 A [struct](../Topic/struct%20\(C%23%20Reference\).md) cannot call a base class constructor; remove the call to the base class constructor.  
  
 The following sample generates CS0522:  
  
```  
// CS0522.cs  
public class clx  
{  
   public clx(int i)  
   {  
   }  
  
   public static void Main()  
   {  
   }  
}  
  
public struct cly  
{  
   public cly(int i):base(0)   // CS0522  
   // try the following line instead  
   // public cly(int i)  
   {  
   }  
}  
```