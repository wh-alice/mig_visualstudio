---
title: "Compiler Error CS1102 | Microsoft Docs"
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
  - "CS1102"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1102"
ms.assetid: 7de798d4-1b4b-4842-ae43-9bc83e6dc9a3
caps.latest.revision: 8
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
# Compiler Error CS1102
The parameter modifier 'out' cannot be used with 'this'.  
  
 When the `this` keyword modifies the first parameter of a static method, it signals to the compiler that the method is an extension method. No other modifiers are needed or allowed on the first parameter of an extension method.  
  
### To correct this error  
  
1.  Remove the unauthorized modifiers from the first parameter.  
  
## Example  
 The following example generates CS1102:  
  
```  
// cs1102.cs  
// Compile with: /target:library.  
public static class Extensions  
{  
    // No type parameters.  
        public static void Test(this out int i) {} // CS1102  
  
    //Single type parameter  
        public static void Test<T>(this out T t) {}// CS1102  
  
    //Multiple type parameters  
        public static void Test<T,U,V>(this out U u) {}// CS1102  
}  
```  
  
## See Also  
 [Extension Methods](/dotnet/csharp/programming-guide/classes-and-structs/extension-methods)   
 [this](/dotnet/csharp/language-reference/keywords/this)   
 [out](/dotnet/csharp/language-reference/keywords/out)