---
title: "CA1712: Do not prefix enum values with type name"
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
  - "CA1712"
  - "DoNotPrefixEnumValuesWithTypeName"
helpviewer_keywords: 
  - "CA1712"
  - "DoNotPrefixEnumValuesWithTypeName"
ms.assetid: df0e3a12-67bf-48f1-a10b-2ef60484a5c7
caps.latest.revision: 15
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
# CA1712: Do not prefix enum values with type name
|||  
|-|-|  
|TypeName|DoNotPrefixEnumValuesWithTypeName|  
|CheckId|CA1712|  
|Category|Microsoft.Naming|  
|Breaking Change|Breaking|  
  
## Cause  
 An enumeration contains a member whose name starts with the type name of the enumeration.  
  
## Rule Description  
 Names of enumeration members are not prefixed with the type name because type information is expected to be provided by development tools.  
  
 Naming conventions provide a common look for libraries that target the common language runtime. This reduces the time that is required for to learn a new software library, and increases customer confidence that the library was developed by someone who has expertise in developing managed code.  
  
## How to Fix Violations  
 To fix a violation of this rule, remove the type name prefix from the enumeration member.  
  
## When to Suppress Warnings  
 Do not suppress a warning from this rule.  
  
## Example  
 The following example shows an incorrectly named enumeration followed by the corrected version.  
  
 [!code[FxCop.Naming.EnumValues#1](../codequality/codesnippet/CSharp/ca1712--do-not-prefix-enum-values-with-type-name_1.cs)]
[!code[FxCop.Naming.EnumValues#1](../codequality/codesnippet/CPP/ca1712--do-not-prefix-enum-values-with-type-name_1.cpp)]
[!code[FxCop.Naming.EnumValues#1](../codequality/codesnippet/VisualBasic/ca1712--do-not-prefix-enum-values-with-type-name_1.vb)]  
  
## Related Rules  
 [CA1711: Identifiers should not have incorrect suffix](../codequality/ca1711--identifiers-should-not-have-incorrect-suffix.md)  
  
 [CA1027: Mark enums with FlagsAttribute](../codequality/ca1027--mark-enums-with-flagsattribute.md)  
  
 [CA2217: Do not mark enums with FlagsAttribute](../codequality/ca2217--do-not-mark-enums-with-flagsattribute.md)  
  
## See Also  
 <xref:System.Enum?displayProperty=fullName>