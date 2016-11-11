---
title: "Operator &#39;&lt;operatorname&gt;&#39; is not defined for types &#39;&lt;typename1&gt;&#39; and &#39;&lt;typename2&gt;&#39; | Microsoft Docs"
ms.custom: ""
ms.date: "2015-07-20"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc31080"
  - "bc31080"
helpviewer_keywords: 
  - "BC31080"
ms.assetid: d2f77450-2bf2-4b1e-b95f-dbc7878f2777
caps.latest.revision: 9
author: "stevehoag"
ms.author: "shoag"
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
# Operator &#39;&lt;operatorname&gt;&#39; is not defined for types &#39;&lt;typename1&gt;&#39; and &#39;&lt;typename2&gt;&#39;
Operator '\<operatorname>' is not defined for types '\<typename1>' and '\<typename2>'. Use 'Is' operator to compare two reference types.  
  
 An attempt was made to use an operator in a way that is inappropriate for the specified types. This error can be caused by using the "=" operator instead of using the `Is` operator to compare two objects.  
  
 **Error ID:** BC31080  
  
### To correct this error  
  
1.  Use `Is` operator to compare two reference types.  
  
2.  Use the `Not` operator in conjunction with the `Is` operator to denote inequality. For example:  
  
     [!code-vb[VbVbalrOOP#89](../misc/codesnippet/VisualBasic/operator-operatorname-is-not-defined-for-types-typename1-and-typename2_1.vb)]  
  
## See Also  
 [Is Operator](/dotnet/visual-basic/language-reference/operators/is-operator)   
 [= Operator](/dotnet/visual-basic/language-reference/operators/assignment-operator)   
 [Not Operator](/dotnet/visual-basic/language-reference/operators/not-operator)