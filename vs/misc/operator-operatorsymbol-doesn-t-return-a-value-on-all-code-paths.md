---
title: "Operator &#39;&lt;operatorsymbol&gt;&#39; doesn&#39;t return a value on all code paths | Microsoft Docs"
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
  - "vbc42106"
  - "bc42106"
helpviewer_keywords: 
  - "BC42106"
ms.assetid: 175b2bc9-5233-462d-97de-9d97b003cc46
caps.latest.revision: 7
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
# Operator &#39;&lt;operatorsymbol&gt;&#39; doesn&#39;t return a value on all code paths
Operator '\<operatorsymbol>' doesn't return a value on all code paths. A null reference exception could occur at run time when the result is used.  
  
 An operator procedure has at least one possible path through its code that does not return a value.  
  
 You can return a value from an operator procedure only by including it in a [Return Statement](/dotnet/visual-basic/language-reference/statements/return-statement).  
  
 If control passes to the `End Operator` statement, the operator procedure returns the default value of the property's data type. For more information, see "Behavior" in [Function Statement](/dotnet/visual-basic/language-reference/statements/function-statement).  
  
 By default, this message is a warning. For more information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../ide/configuring-warnings-in-visual-basic.md).  
  
 **Error ID:** BC42106  
  
### To correct this error  
  
-   Check your control flow logic and make sure every possible path ends with a `Return` statement. In particular, the last statement before `End Operator` should be a `Return` statement.  
  
## See Also  
 [Operator Procedures](/dotnet/visual-basic/language-reference/procedures/operator-procedures)   
 [Operator Statement](/dotnet/visual-basic/language-reference/statements/operator-statement)