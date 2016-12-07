---
title: "CA1301: Avoid duplicate accelerators"
ms.custom: ""
ms.date: "12/07/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-devops-test"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CA1301"
  - "AvoidDuplicateAccelerators"
helpviewer_keywords: 
  - "CA1301"
  - "AvoidDuplicateAccelerators"
ms.assetid: 20570a00-864b-459c-a1fa-a6e9db5f1001
caps.latest.revision: 17
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
# CA1301: Avoid duplicate accelerators
[!INCLUDE[vs2017banner](../code-quality/includes/vs2017banner.md)]

|||  
|-|-|  
|TypeName|AvoidDuplicateAccelerators|  
|CheckId|CA1301|  
|Category|Microsoft.Globalization|  
|Breaking Change|Non-breaking|  
  
## Cause  
 A type extends <xref:System.Windows.Forms.Control?displayProperty=fullName> and contains two or more top level controls that have identical access keys that are stored in a resource file.  
  
## Rule Description  
 An access key, also known as an accelerator, enables keyboard access to a control by using the ALT key. When multiple controls have duplicate access keys, the behavior of the access key is not well defined. The user might not be able to access the intended control by using the access key and a control other than the one that is intended might be enabled.  
  
 The current implementation of this rule ignores menu items. However, menu items in the same submenu should not have identical access keys.  
  
## How to Fix Violations  
 To fix a violation of this rule, define unique access keys for all controls.  
  
## When to Suppress Warnings  
 Do not suppress a warning from this rule.  
  
## Example  
 The following example shows a minimal form that contains two controls that have identical access keys. The keys are stored in a resource file, which is not shown; however, their values appear in the commented out `checkBox.Text` lines. The behavior of duplicate accelerators can be examined by exchanging the `checkBox.Text` lines with their commented out counterparts. However, in this case, the example will not generate a warning from the rule.  
  
 [!code-cs[FxCop.Globalization.AvoidDuplicateAccels#1](../code-quality/codesnippet/CSharp/ca1301--avoid-duplicate-accelerators_1.cs)]  
  
## See Also  
 <xref:System.Resources.ResourceManager?displayProperty=fullName>   
 [Resources in Desktop Apps](http://msdn.microsoft.com/library/8ad495d4-2941-40cf-bf64-e82e85825890)