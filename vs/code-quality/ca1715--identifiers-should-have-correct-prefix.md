---
title: "CA1715: Identifiers should have correct prefix | Microsoft Docs"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-devops-test"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CA1715"
  - "IdentifiersShouldHaveCorrectPrefix"
helpviewer_keywords: 
  - "IdentifiersShouldHaveCorrectPrefix"
  - "CA1715"
ms.assetid: cf45f8df-6855-4cb6-a4e2-7cfed714cf2f
caps.latest.revision: 30
ms.author: "douge"
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
# CA1715: Identifiers should have correct prefix
|||  
|-|-|  
|TypeName|IdentifiersShouldHaveCorrectPrefix|  
|CheckId|CA1715|  
|Category|Microsoft.Naming|  
|Breaking Change|Breaking - when fired on interfaces.<br /><br /> Non-breaking - when raised on generic type parameters.|  
  
## Cause  
 The name of an externally visible interface does not start with an uppercase 'I'.  
  
 -or-  
  
 The name of a generic type parameter on an externally visible type or method does not start with an uppercase 'T'.  
  
## Rule Description  
 By convention, the names of certain programming elements start with a specific prefix.  
  
 Interface names should start with an uppercase 'I' followed by another uppercase letter. This rule reports violations for interface names such as 'MyInterface' and 'IsolatedInterface'.  
  
 Generic type parameter names should start with an uppercase 'T' and optionally may be followed by another uppercase letter. This rule reports violations for generic type parameter names such as 'V' and 'Type'.  
  
 Naming conventions provide a common look for libraries that target the common language runtime. This reduces the learning curve that is required for new software libraries, and increases customer confidence that the library was developed by someone who has expertise in developing managed code.  
  
## How to Fix Violations  
 Rename the identifier so that it is correctly prefixed.  
  
## When to Suppress Warnings  
 Do not suppress a warning from this rule.  
  
## Example  
 **The following example shows an incorrectly named interface.**  
  
 [!CODE [FxCop.Naming.IdentifiersShouldHaveCorrectPrefix#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Naming.IdentifiersShouldHaveCorrectPrefix#1)]  
  
## Example  
 **The following example fixes the previous violation by prefixing the interface with 'I'.**  
  
 [!CODE [FxCop.Naming.IdentifiersShouldHaveCorrectPrefix2#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Naming.IdentifiersShouldHaveCorrectPrefix2#1)]  
  
## Example  
 **The following example shows an incorrectly named generic type parameter.**  
  
 [!CODE [FxCop.Naming.IdentifiersShouldHaveCorrectPrefix3#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Naming.IdentifiersShouldHaveCorrectPrefix3#1)]  
  
## Example  
 **The following example fixes the previous violation by prefixing the generic type parameter with 'T'.**  
  
 [!CODE [FxCop.Naming.IdentifiersShouldHaveCorrectPrefix4#1](../CodeSnippet/VS_Snippets_CodeAnalysis/FxCop.Naming.IdentifiersShouldHaveCorrectPrefix4#1)]  
  
## Related Rules  
 [CA1722: Identifiers should not have incorrect prefix](../code-quality/ca1722--identifiers-should-not-have-incorrect-prefix.md)