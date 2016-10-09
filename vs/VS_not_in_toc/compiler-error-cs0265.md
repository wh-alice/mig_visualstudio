---
title: "Compiler Error CS0265"
ms.custom: na
ms.date: "10/01/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "CS0265"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0265"
ms.assetid: d43d19c2-8a66-4bb1-95a0-557b0a29bce1
caps.latest.revision: 11
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
# Compiler Error CS0265
Partial declarations of 'type' have inconsistent constraints for type parameter 'type parameter'  
  
 This error happens when you define a generic class as a partial class, so that its partial definitions occur in more than one place, and the constraints on the generic type are inconsistent or different in two or more places. If you specify the constraints in more than one place, they must all be identical. The easiest solution is to specify the constraints in one place, and omit them everywhere else. For more information, see [Partial Classes and Methods](../Topic/Partial%20Classes%20and%20Methods%20\(C%23%20Programming%20Guide\).md) and [Constraints on Type Parameters](../Topic/Constraints%20on%20Type%20Parameters%20\(C%23%20Programming%20Guide\).md).  
  
 The following code generates error CS0265.  
  
## Example  
 In this code, the partial class definitions are all in a single file, but they could also be spread across multiple files.  
  
```  
// CS0265.cs  
public class GenericsErrors   
{  
    interface IFace1 { }  
    interface IFace2 { }  
    partial class PartialBadBounds<T> where T : IFace1 { } // CS0265  
    partial class PartialBadBounds<T> where T : IFace2 { }   
}  
```