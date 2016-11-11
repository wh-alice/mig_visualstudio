---
title: "Compiler Error CS1529 | Microsoft Docs"
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
  - "CS1529"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1529"
ms.assetid: 672a6fd1-3a1f-422c-a29f-46f196d15211
caps.latest.revision: 10
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
# Compiler Error CS1529
A using clause must precede all other elements defined in the namespace except extern alias declarations  
  
 A [using](/dotnet/csharp/language-reference/keywords/using) clause must appear first in a namespace.  
  
## Example  
 The following sample generates CS1529:  
  
```  
// CS1529.cs  
namespace X  
{  
    namespace Subspace  
    {  
        using Microsoft;  
  
        class SomeClass  
        {  
        };  
  
        using Microsoft;      // CS1529, place before class definition  
    }  
  
    using System.Reflection;  // CS1529, place before namespace 'Subspace'  
}  
  
using System;                 // CS1529, place at the beginning of the file  
```