---
title: "Compiler Error CS0227 | Microsoft Docs"
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
  - "CS0227"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0227"
ms.assetid: b595a1c9-8204-4ff7-a1d0-258b0b1d6ff7
caps.latest.revision: 11
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
# Compiler Error CS0227
Unsafe code may only appear if compiling with /unsafe  
  
 If source code contains the [unsafe](/dotnet/csharp/language-reference/keywords/unsafe) keyword, then the [/unsafe](/dotnet/csharp/language-reference/compiler-options/unsafe-compiler-option) compiler option must also be used. For more information, see [Unsafe Code and Pointers](/dotnet/csharp/programming-guide/unsafe-code-pointers/index).  
  
 To set the unsafe option in [!INCLUDE[vs_current_long](../misc/includes/vs_current_long_md.md)], click on **Project** in the main menu, select the **Build** pane, and check the box that says "allow unsafe code."  
  
 The following sample, when compiled without **/unsafe**, will generate CS0227:  
  
```  
// CS0227.cs  
public class MyClass  
{  
   unsafe public static void Main()   // CS0227  
   {  
   }  
}  
```  
  
## See Also  
 [C# Compiler Errors](/dotnet/csharp/language-reference/compiler-messages/index)