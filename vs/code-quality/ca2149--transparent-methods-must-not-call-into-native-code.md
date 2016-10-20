---
title: "CA2149: Transparent methods must not call into native code | Microsoft Docs"
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
  - "CA2149"
ms.assetid: 28951bd7-f3db-4871-99aa-bad68d1ead80
caps.latest.revision: 11
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
# CA2149: Transparent methods must not call into native code
|||  
|-|-|  
|TypeName|TransparentMethodsMustNotCallNativeCode|  
|CheckId|CA2149|  
|Category|Microsoft.Security|  
|Breaking Change|Breaking|  
  
## Cause  
 A method calls a native function through a method stub such as P/Invoke.  
  
## Rule Description  
 This rule fires on any transparent method which calls directly into native code, for example, through a P/Invoke. Violations of this rule lead to a <xref:System.MethodAccessException> in the level 2 transparency model, and a full demand for <xref:System.Security.Permissions.SecurityPermissionAttribute.UnmanagedCode*> in the level 1 transparency model.  
  
## How to Fix Violations  
 To fix a violation of this rule, mark the method that calls the native code with the <xref:System.Security.SecurityCriticalAttribute> or <xref:System.Security.SecuritySafeCriticalAttribute> attribute.  
  
## When to Suppress Warnings  
 Do not suppress a warning from this rule.  
  
## Example  
 [!CODE [FxCop.Security.CA2149.TransparentMethodsMustNotCallNativeCode#1](../CodeSnippet/VS_Snippets_CodeAnalysis/fxcop.security.ca2149.transparentmethodsmustnotcallnativecode#1)]