---
title: "Compiler Error CS1106 | Microsoft Docs"
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
  - "CS1106"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1106"
ms.assetid: 3585600a-6b2c-47aa-a418-ef049f07c107
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
# Compiler Error CS1106
Extension methods must be defined in a non generic static class.  
  
 Extension methods must be defined as static methods in a non-generic static class.  
  
## Example  
 The following example generates CS1106 because the class `Extensions` is not defined as `static`:  
  
```  
// cs1106.cs  
public class Extensions // CS1106  
{  
    public  static void Test<T>(this System.String s) {}  
}  
```  
  
## See Also  
 [Extension Methods](/dotnet/csharp/programming-guide/classes-and-structs/extension-methods)   
 [static](/dotnet/csharp/language-reference/keywords/static)