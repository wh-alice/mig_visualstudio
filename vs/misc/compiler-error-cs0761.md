---
title: "Compiler Error CS0761"
ms.custom: ""
ms.date: "10/25/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0761"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0761"
ms.assetid: b16ac1df-0ddc-44d2-89f1-8d9c32af87ad
caps.latest.revision: 5
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
# Compiler Error CS0761
Partial method declarations of 'method\<T>' have inconsistent type parameter constraints.  
  
 If a partial method has an implementation, the generic type constraint must be identical to the constraint defined on the method signature.  
  
### To correct this error  
  
1.  Make the generic type constraints identical on each part of the partial method.  
  
## Example  
 The following code generates CS0761:  
  
```  
// cs0761.cs  
using System;  
  
public partial class C  
{  
    partial void Part<T>() where T : class;  
    partial void Part<T>() where T : struct // CS0761  
    {  
    }  
  
    public static int Main()  
    {  
        return 1;  
    }  
}  
  
```  
  
## See Also  
 [Partial Classes and Methods](../Topic/Partial%20Classes%20and%20Methods%20\(C%23%20Programming%20Guide\).md)   
 [Constraints on Type Parameters](../Topic/Constraints%20on%20Type%20Parameters%20\(C%23%20Programming%20Guide\).md)