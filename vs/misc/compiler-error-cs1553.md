---
title: "Compiler Error CS1553 | Microsoft Docs"
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
  - "CS1553"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1553"
ms.assetid: aec64251-b4ac-45c0-b143-7ebda138af6e
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
# Compiler Error CS1553
Declaration is not valid; use 'modifier operator \<dest-type> (...' instead  
  
 The return type for an [operator](/dotnet/csharp/language-reference/keywords/operator) must immediately precede the parameter list, and *modifier* is either `implicit` or **explicit**.  
  
 The following sample generates CS1553:  
  
```  
// CS1553.cs  
class MyClass  
{  
   public static int implicit operator (MyClass f)   // CS1553  
   // try the following line instead  
   // public static implicit operator int (MyClass f)  
   {  
      return 6;  
   }  
  
   public static void Main()  
   {  
   }  
}  
```