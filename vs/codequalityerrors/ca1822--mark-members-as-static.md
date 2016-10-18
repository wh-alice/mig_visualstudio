---
title: "CA1822: Mark members as static"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-devops-test"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "MarkMembersAsStatic"
  - "CA1822"
helpviewer_keywords: 
  - "MarkMembersAsStatic"
  - "CA1822"
ms.assetid: 743f0af7-41d1-4852-8d97-af0688b31118
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
# CA1822: Mark members as static
|||  
|-|-|  
|TypeName|MarkMembersAsStatic|  
|CheckId|CA1822|  
|Category|Microsoft.Performance|  
|Breaking Change|Non-breaking - If the member is not visible outside the assembly, regardless of the change you make. Non Breaking - If you just change the member to an instance member with the `this` keyword.<br /><br /> Breaking - If you change the member from an instance member to a static member and it is visible outside the assembly.|  
  
## Cause  
 A member that does not access instance data is not marked as static (Shared in [!INCLUDE[vbprvb](../codequality/includes/vbprvb_md.md)]).  
  
## Rule Description  
 Members that do not access instance data or call instance methods can be marked as static (Shared in [!INCLUDE[vbprvb](../codequality/includes/vbprvb_md.md)]). After you mark the methods as static, the compiler will emit nonvirtual call sites to these members. Emitting nonvirtual call sites will prevent a check at runtime for each call that makes sure that the current object pointer is non-null. This can achieve a measurable performance gain for performance-sensitive code. In some cases, the failure to access the current object instance represents a correctness issue.  
  
## How to Fix Violations  
 Mark the member as static (or Shared in [!INCLUDE[vbprvb](../codequality/includes/vbprvb_md.md)]) or use 'this'/'Me' in the method body, if appropriate.  
  
## When to Suppress Warnings  
 It is safe to suppress a warning from this rule for previously shipped code for which the fix would be a breaking change.  
  
## Related Rules  
 [CA1811: Avoid uncalled private code](../codequality/ca1811--avoid-uncalled-private-code.md)  
  
 [CA1812: Avoid uninstantiated internal classes](../codequality/ca1812--avoid-uninstantiated-internal-classes.md)  
  
 [CA1804: Remove unused locals](../codequality/ca1804--remove-unused-locals.md)