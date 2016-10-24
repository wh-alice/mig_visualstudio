---
title: "CA1719: Parameter names should not match member names | testtitle"
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
  - "ParameterNamesShouldNotMatchMemberNames"
  - "CA1719"
helpviewer_keywords: 
  - "CA1719"
  - "ParameterNamesShouldNotMatchMemberNames"
ms.assetid: c6fea690-1659-4ee7-a1c5-125ad6754525
caps.latest.revision: 18
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
# CA1719: Parameter names should not match member names
|||  
|-|-|  
|TypeName|ParameterNamesShouldNotMatchMemberNames|  
|CheckId|CA1719|  
|Category|Microsoft.Naming|  
|Breaking Change|Breaking|  
  
## Cause  
 The name of an externally visible member matches, in a case-insensitive comparison, the name of one of its parameters.  
  
## Rule Description  
 A parameter name should communicate the meaning of a parameter and a member name should communicate the meaning of a member. It would be a rare design where these were the same. Naming a parameter the same as its member name is unintuitive and makes the library difficult to use.  
  
## How to Fix Violations  
 Select a parameter name that does not match the member name.  
  
## When to Suppress Warnings  
 For new development, no known scenarios occur where you must suppress a warning from this rule. For shipping libraries, you might have to suppress a warning from this rule.  
  
## Related Rules  
 [CA1709: Identifiers should be cased correctly](../code-quality/ca1709--identifiers-should-be-cased-correctly.md)  
  
 [CA1708: Identifiers should differ by more than case](../code-quality/ca1708--identifiers-should-differ-by-more-than-case.md)  
  
 [CA1707: Identifiers should not contain underscores](../code-quality/ca1707--identifiers-should-not-contain-underscores.md)