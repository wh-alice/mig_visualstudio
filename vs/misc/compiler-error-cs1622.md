---
title: "Compiler Error CS1622 | Microsoft Docs"
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
  - "CS1622"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1622"
ms.assetid: 6b53a777-4cd8-423a-84ff-22ff588044d3
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
# Compiler Error CS1622
Cannot return a value from an iterator. Use the yield return statement to return a value, or yield break to end the iteration.  
  
 An iterator is a special function that returns a value via the yield statement rather than the return statement. For more information, see **iterators**.  
  
 The following sample generates CS1622:  
  
```  
// CS1622.cs  
// compile with: /target:library  
using System.Collections;  
  
class C : IEnumerable  
{  
   public IEnumerator GetEnumerator()  
   {  
      return (IEnumerator) this;  // CS1622  
      yield return this;   // OK  
   }  
}  
```