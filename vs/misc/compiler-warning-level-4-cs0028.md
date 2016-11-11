---
title: "Compiler Warning (level 4) CS0028 | Microsoft Docs"
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
  - "CS0028"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0028"
ms.assetid: 47df919f-01fa-45ae-a4b7-912445e679e2
caps.latest.revision: 15
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
# Compiler Warning (level 4) CS0028
'function declaration' has the wrong signature to be an entry point  
  
 The method declaration for `Main` was invalid: it was declared with an invalid signature. `Main` must be declared as static and it must return either [int](/dotnet/csharp/language-reference/keywords/int) or [void](/dotnet/csharp/language-reference/keywords/void). For more information, see [Main() and Command-Line Arguments](/dotnet/csharp/programming-guide/main-and-command-args/main-and-command-line-arguments).  
  
 The following sample generates CS0028:  
  
```  
// CS0028.cs  
// compile with: /W:4 /warnaserror  
public class a  
{  
    public static double Main(int i)   // CS0028  
    // Try the following line instead:  
    // public static void Main()  
    {  
    }  
}  
```