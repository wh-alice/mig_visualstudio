---
title: "CA2231: Overload operator equals on overriding ValueType.Equals | hehe"
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
  - "OverloadOperatorEqualsOnOverridingValueTypeEquals"
  - "CA2231"
  - "OverrideOperatorEqualsOnOverridingValueTypeEquals"
helpviewer_keywords: 
  - "OverloadOperatorEqualsOnOverridingValueTypeEquals"
  - "CA2231"
ms.assetid: 114c0161-261a-40ad-8b2c-0932d6909d2a
caps.latest.revision: 17
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
# CA2231: Overload operator equals on overriding ValueType.Equals
|||  
|-|-|  
|TypeName|OverloadOperatorEqualsOnOverridingValueTypeEquals|  
|CheckId|CA2231|  
|Category|Microsoft.Usage|  
|Breaking Change|Non Breaking|  
  
## Cause  
 A value type overrides <xref:System.Object.Equals*?displayProperty=fullName> but does not implement the equality operator.  
  
## Rule Description  
 In most programming languages there is no default implementation of the equality operator (==) for value types. If your programming language supports operator overloads, you should consider implementing the equality operator. Its behavior should be identical to that of <xref:System.Object.Equals*>.  
  
 You cannot use the default equality operator in an overloaded implementation of the equality operator. Doing so will cause a stack overflow. To implement the equality operator, use the Object.Equals method in your implementation. For example:  
  
```vb  
If (Object.ReferenceEquals(left, Nothing)) Then  
    Return Object.ReferenceEquals(right, Nothing)  
Else  
    Return left.Equals(right)  
End If  
```  
  
```c#  
if (Object.ReferenceEquals(left, null))   
    return Object.ReferenceEquals(right, null);  
return left.Equals(right);  
```  
  
## How to Fix Violations  
 To fix a violation of this rule, implement the equality operator.  
  
## When to Suppress Warnings  
 It is safe to suppress a warning from this rule; however, we recommend that you provide the equality operator if possible.  
  
## Example  
 The following example defines a type that violates this rule.  
  
 [!code[FxCop.Usage.EqualsGetHashCode#1](../code-quality/codesnippet/CSharp/ca2231--overload-operator-equals-on-overriding-valuetype.equals_1.cs)]  
  
## Related Rules  
 [CA1046: Do not overload operator equals on reference types](../code-quality/ca1046--do-not-overload-operator-equals-on-reference-types.md)  
  
 [CA2225: Operator overloads have named alternates](../code-quality/ca2225--operator-overloads-have-named-alternates.md)  
  
 [CA2226: Operators should have symmetrical overloads](../code-quality/ca2226--operators-should-have-symmetrical-overloads.md)  
  
 [CA2224: Override equals on overloading operator equals](../code-quality/ca2224--override-equals-on-overloading-operator-equals.md)  
  
 [CA2218: Override GetHashCode on overriding Equals](../code-quality/ca2218--override-gethashcode-on-overriding-equals.md)  
  
## See Also  
 <xref:System.Object.Equals*?displayProperty=fullName>