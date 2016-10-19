---
title: "CA2143: Transparent methods should not use security demands"
ms.custom: ""
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-devops-test"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CA2143"
ms.assetid: 5d3923d7-cf40-4512-bc5c-0db0e0d6e25a
caps.latest.revision: 12
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
# CA2143: Transparent methods should not use security demands
|||  
|-|-|  
|TypeName|TransparentMethodsShouldNotDemand|  
|CheckId|CA2143|  
|Category|Microsoft.Security|  
|Breaking Change|Breaking|  
  
## Cause  
 A tranparent type or method is declaratively marked with a <xref:System.Security.Permissions.SecurityAction?displayProperty=fullName>`.Demand` demand or the method calls the <xref:System.Security.CodeAccessPermission.Demand*?displayProperty=fullName> method.  
  
## Rule Description  
 Security transparent code should not be responsible for verifying the security of an operation, and therefore should not demand permissions. Security transparent code should use full demands to make security decisions and safe-critical code should not rely on transparent code to have made the full demand. Any code that performs security checks, such as security demands, should be safe-critical instead.  
  
## How to Fix Violations  
 In general, to fix a violation of this rule, mark the method with the <xref:System.Security.SecuritySafeCriticalAttribute> attribute. You can also remove the demand.  
  
## When to Suppress Warnings  
 Do not suppress a warning from this rule.  
  
## Example  
 The rule files on the following code because a transparent method makes a declarative security demand.  
  
 [!code[FxCop.Security.CA2143.TransparentMethodsShouldNotDemand#1](../codequality/codesnippet/CSharp/ca2143--transparent-methods-should-not-use-security-demands_1.cs)]  
  
## See Also  
 [CA2142: Transparent code should not be protected with LinkDemands](../codequality/ca2142--transparent-code-should-not-be-protected-with-linkdemands.md)