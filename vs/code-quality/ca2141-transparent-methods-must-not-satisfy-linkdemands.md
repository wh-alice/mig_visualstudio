---
title: "CA2141:Transparent methods must not satisfy LinkDemands | testtitle"
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
  - "CA2141"
ms.assetid: 2957f5f7-c511-4180-ba80-752034f10a77
caps.latest.revision: 14
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
# CA2141:Transparent methods must not satisfy LinkDemands
|||  
|-|-|  
|TypeName|TransparentMethodsMustNotSatisfyLinkDemands|  
|CheckId|CA2141|  
|Category|Microsoft.Security|  
|Breaking Change|Breaking|  
  
## Cause  
 A security transparent method calls a method in an assembly that is not marked with the <xref:System.Security.AllowPartiallyTrustedCallersAttribute> (APTCA) attribute, or a security transparent method satisfies a <xref:System.Security.Permissions.SecurityAction>`.LinkDemand` for a type or a method.  
  
## Rule Description  
 Satisfying a LinkDemand is a security sensitive operation which can cause unintentional elevation of privilege. Security transparent code must not satisfy LinkDemands, because it is not subject to the same security audit requirements as security critical code. Transparent methods in security rule set level 1 assemblies will cause all LinkDemands they satisfy to be converted to full demands at run time, which can cause performance problems. In security rule set level 2 assemblies, transparent methods will fail to compile in the just-in-time (JIT) compiler if they attempt to satisfy a LinkDemand.  
  
 In assemblies that usee Level 2 security, attempts by a security transparent method to satisfy a LinkDemand or call a method in a non-APTCA assembly raises a <xref:System.MethodAccessException>; in Level 1 assemblies the LinkDemand becomes a full Demand.  
  
## How to Fix Violations  
 To fix a violation of this rule, mark the accessing method with the <xref:System.Security.SecurityCriticalAttribute> or <xref:System.Security.SecuritySafeCriticalAttribute> attribute, or remove the LinkDemand from the accessed method.  
  
## When to Suppress Warnings  
 Do not suppress a warning from this rule.  
  
## Example  
 In this example, a transparent method attempts to call a method that has a LinkDemand. This rule will fire on this code.  
  
 [!code[FxCop.Security.CA2141.TransparentMethodsMustNotSatisfyLinkDemands#1](../code-quality/codesnippet/CSharp/ca2141-transparent-methods-must-not-satisfy-linkdemands_1.cs)]