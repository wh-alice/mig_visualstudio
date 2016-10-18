---
title: "CA1714: Flags enums should have plural names"
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
  - "FlagsEnumsShouldHavePluralNames"
  - "CA1714"
helpviewer_keywords: 
  - "CA1714"
  - "FlagsEnumsShouldHavePluralNames"
ms.assetid: 95ef5b43-7681-49e9-a5a3-ac0357cf1be7
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
# CA1714: Flags enums should have plural names
|||  
|-|-|  
|TypeName|FlagsEnumsShouldHavePluralNames|  
|CheckId|CA1714|  
|Category|Microsoft.Naming|  
|Breaking Change|Breaking|  
  
## Cause  
 A public enumeration has the <xref:System.FlagsAttribute?displayProperty=fullName> and its name does not end in 's'.  
  
## Rule Description  
 Types that are marked with <xref:System.FlagsAttribute> have names that are plural because the attribute indicates that more than one value can be specified. For example, an enumeration that defines the days of the week might be intended for use in an application where you can specify multiple days. This enumeration should have the <xref:System.FlagsAttribute> and could be called 'Days'. A similar enumeration that allows only a single day to be specified would not have the attribute, and could be called 'Day'.  
  
 Naming conventions provide a common look for libraries that target the common language runtime. This reduces the learning curve that is required for new software libraries, and increases customer confidence that the library was developed by someone who has expertise in developing managed code.  
  
## How to Fix Violations  
 Make the name of the enumeration a plural word, or remove the <xref:System.FlagsAttribute> attribute if multiple enumeration values should not be specified simultaneously.  
  
## When to Suppress Warnings  
 It is safe to suppress a violation if the name is a plural word but does not end in 's'. For example, if the multiple-day enumeration that was described previously were named 'DaysOfTheWeek', this would violate the logic of the rule but not its intent. Such violations should be suppressd.  
  
## Related Rules  
 [CA1027: Mark enums with FlagsAttribute](../codequality/ca1027--mark-enums-with-flagsattribute.md)  
  
 [CA2217: Do not mark enums with FlagsAttribute](../codequality/ca2217--do-not-mark-enums-with-flagsattribute.md)  
  
## See Also  
 <xref:System.FlagsAttribute?displayProperty=fullName>   
 [Enum Design](../Topic/Enum%20Design.md)