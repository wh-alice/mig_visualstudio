---
title: "CA2137: Transparent methods must contain only verifiable IL"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-devops-test"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "CA2137"
ms.assetid: cbaeb0e1-56b6-43b4-812a-596b2859c329
caps.latest.revision: 13
ms.author: "douge"
manager: "douge"
translation.priority.ht: 
  - "cs-cz"
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "pl-pl"
  - "pt-br"
  - "ru-ru"
  - "tr-tr"
  - "zh-cn"
  - "zh-tw"
---
# CA2137: Transparent methods must contain only verifiable IL
|||  
|-|-|  
|TypeName|TransparentMethodsMustBeVerifiable|  
|CheckId|CA2137|  
|Category|Microsoft.Security|  
|Breaking Change|Breaking|  
  
## Cause  
 A method contains unverifiable code or returns a type by reference.  
  
## Rule Description  
 This rule fires on attempts by security transparent code to execute unverifiable MSIL (Microsoft Intermediate Language). However, the rule does not contain a full IL verifier, and instead uses heuristics to catch most violations of MSIL verification.  
  
 To be certain that your code contains only verifiable MSIL, run [Peverify.exe (PEVerify Tool)](../Topic/Peverify.exe%20\(PEVerify%20Tool\).md) on your assembly. Run PEVerify with the **/transparent** option which limits the output to only unverifiable transparent methods which would cause an error. If the /transparent option is not used, PEVerify also verifies critical methods that are allowed to contain unverifiable code.  
  
## How to Fix Violations  
 To fix a violation of this rule, mark the method with the \<xref:System.Security.SecurityCriticalAttribute> or \<xref:System.Security.SecuritySafeCriticalAttribute> attribute, or remove the unverifiable code.  
  
## When to Suppress Warnings  
 Do not suppress a warning from this rule.  
  
## Example  
 The method in this example uses unverifiable code and should be marked with the \<xref:System.Security.SecurityCriticalAttribute> or \<xref:System.Security.SecuritySafeCriticalAttribute> attribute.  
  
 [!code[FxCop.Security.CA2137.TransparentMethodsMustBeVerifiable#1](../VS_IDE/codesnippet/CSharp/ca2137--transparent-methods-must-contain-only-verifiable-il_1.cs)]