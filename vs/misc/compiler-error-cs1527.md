---
title: "Compiler Error CS1527 | Microsoft Docs"
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
  - "CS1527"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1527"
ms.assetid: a0d52130-d6da-41bb-b153-8e96cbb7e316
caps.latest.revision: 9
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
# Compiler Error CS1527
Elements defined in a namespace cannot be explicitly declared as private, protected, or protected internal  
  
 Type declarations in a namespace can have either [public](/dotnet/csharp/language-reference/keywords/public) or [internal](/dotnet/csharp/language-reference/keywords/internal) access. If no accessibility is specified, **internal** is the default.  
  
 The following sample generates CS1527:  
  
```  
// CS1527.cs  
namespace Sample  
{  
   private class C1 {};             // CS1527  
   protected class C2 {};           // CS1527  
   protected internal class C3 {};  // CS1527  
}  
```  
  
 The following example generates CS1527 because when no namespace is explicitly declared in your program code, all type declarations are located implicitly within the global namespace.  
  
```  
//cs1527_2.cs  
using System;  
  
protected class C4{}  
private struct S1{}  
```  
  
## See Also  
 [Namespaces](/dotnet/csharp/programming-guide/namespaces/index)   
 [global](/dotnet/csharp/language-reference/keywords/global)   
 [:: Operator](http://msdn.microsoft.com/en-us/Library/698b5a73-85cf-4e0e-9e8e-6496887f8527)   
 [Accessibility Domain](/dotnet/csharp/language-reference/keywords/accessibility-domain)   
 [Access Modifiers](/dotnet/csharp/programming-guide/classes-and-structs/access-modifiers)