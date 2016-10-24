---
title: "Compiler Error CS1944"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS1944"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1944"
ms.assetid: e5e2c018-9a7e-48ee-8dd3-98e3553777c1
caps.latest.revision: 8
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
# Compiler Error CS1944
An expression tree may not contain an unsafe pointer operation  
  
 Expression trees do not support pointer types because the <xref:System.Linq.Expressions.Expression`1.Compile*?displayProperty=fullName> method is only allowed to produce verifiable code. See comments.  
  
### To correct this error  
  
1.  Do not use pointer types when you are trying to create an expression tree.  
  
## Example  
 The following example generates CS1944:  
  
<CodeContentPlaceHolder>0</CodeContentPlaceHolder>  
 In some situations it is okay to have pointers in expression trees. For example, consider the following code:  
  
 `Expression<Func\<int*[], int*[]>) e = (int*[] i)=>i;`  
  
 This code is a valid expression tree because no type arguments are pointer types. They are arrays of pointers, and arrays are not pointer types. Also, the body of the expression tree does not do anything dangerous with any pointer.  
  
## See Also  
 [unsafe](../Topic/unsafe%20\(C%23%20Reference\).md)