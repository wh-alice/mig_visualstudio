---
title: "Compiler Error CS0706 | Microsoft Docs"
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
  - "CS0706"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0706"
ms.assetid: bc3ac5c0-8c96-43c8-b10a-69bd31b38e4a
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
# Compiler Error CS0706
Invalid constraint type. A type used as a constraint must be an interface, a non-sealed class or a type parameter.  
  
 This error occurs when an invalid construct is used in a constraint clause. To avoid this error, use an interface or non-sealed class instead of the construct that caused the error.  
  
## Example  
 The following sample generates CS0706.  
  
```  
// CS0706.cs  
// compile with: /target:library  
class A {}  
class C<T> where T : int[] {}  // CS0706  
class D<T> where T : A {}  // OK  
```