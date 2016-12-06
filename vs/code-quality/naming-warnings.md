---
title: "Naming Warnings"
ms.custom: ""
ms.date: "12/05/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-devops-test"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vs.codeanalysis.namingrules"
helpviewer_keywords: 
  - "managed code analysis warnings, naming warnings"
  - "naming warnings"
  - "warnings, naming"
ms.assetid: f97223ce-1d39-4134-81c9-fff2c75d979b
caps.latest.revision: 19
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
# Naming Warnings
[!INCLUDE[vs2017banner](../code-quality/includes/vs2017banner.md)]

Naming warnings support adherence to the naming conventions of the [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] Design Guidelines.  
  
## In This Section  
  
|Rule|Description|  
|----------|-----------------|  
|[CA1700: Do not name enum values 'Reserved'](../code-quality/ca1700--do-not-name-enum-values--reserved-.md)|This rule assumes that an enumeration member that has a name that contains "reserved" is not currently used but is a placeholder to be renamed or removed in a future version. Renaming or removing a member is a breaking change.|  
|[CA1713: Events should not have before or after prefix](../code-quality/ca1713--events-should-not-have-before-or-after-prefix.md)|The name of an event starts with "Before" or "After". To name related events that are raised in a specific sequence, use the present or past tense to indicate the relative position in the sequence of actions.|  
|[CA1714: Flags enums should have plural names](../code-quality/ca1714--flags-enums-should-have-plural-names.md)|A public enumeration has the System.FlagsAttribute attribute and its name does not end in "s". Types that are marked with FlagsAttribute have names that are plural because the attribute indicates that more than one value can be specified.|  
|[CA1704: Identifiers should be spelled correctly](../code-quality/ca1704--identifiers-should-be-spelled-correctly.md)|The name of an externally visible identifier contains one or more words that are not recognized by the Microsoft spelling checker library.|  
|[CA1708: Identifiers should differ by more than case](../code-quality/ca1708--identifiers-should-differ-by-more-than-case.md)|Identifiers for namespaces, types, members, and parameters cannot differ only by case because languages that target the common language runtime are not required to be case-sensitive.|  
|[CA1715: Identifiers should have correct prefix](../code-quality/ca1715--identifiers-should-have-correct-prefix.md)|The name of an externally visible interface does not start with a capital "I".  The name of a generic type parameter on an externally visible type or method does not start with a capital "T".|  
|[CA1720: Identifiers should not contain type names](../code-quality/ca1720--identifiers-should-not-contain-type-names.md)|The name of a parameter in an externally visible member contains a data type name, or the name of an externally visible member contains a language-specific data type name.|  
|[CA1722: Identifiers should not have incorrect prefix](../code-quality/ca1722--identifiers-should-not-have-incorrect-prefix.md)|By convention, only certain programming elements have names that begin with a specific prefix.|  
|[CA1711: Identifiers should not have incorrect suffix](../code-quality/ca1711--identifiers-should-not-have-incorrect-suffix.md)|By convention, only the names of types that extend certain base types or that implement certain interfaces, or types that are derived from these types, should end with specific reserved suffixes. Other type names should not use these reserved suffixes.|  
|[CA1717: Only FlagsAttribute enums should have plural names](../code-quality/ca1717--only-flagsattribute-enums-should-have-plural-names.md)|Naming conventions dictate that a plural name for an enumeration indicates that more than one value of the enumeration can be specified at the same time.|  
|[CA1725: Parameter names should match base declaration](../code-quality/ca1725--parameter-names-should-match-base-declaration.md)|Consistent naming of parameters in an override hierarchy increases the usability of the method overrides. A parameter name in a derived method that differs from the name in the base declaration can cause confusion about whether the method is an override of the base method or a new overload of the method.|  
|[CA1719: Parameter names should not match member names](../code-quality/ca1719--parameter-names-should-not-match-member-names.md)|A parameter name should communicate the meaning of a parameter, and a member name should communicate the meaning of a member. It would be a rare design where these were the same. Naming a parameter the same as its member name is unintuitive and makes the library difficult to use.|  
|[CA1701: Resource string compound words should be cased correctly](../code-quality/ca1701--resource-string-compound-words-should-be-cased-correctly.md)|Each word in the resource string is split into tokens that are based on the casing. Each contiguous two-token combination is checked by the Microsoft spelling checker library. If recognized, the word produces a violation of the rule.|  
|[CA1703: Resource strings should be spelled correctly](../code-quality/ca1703--resource-strings-should-be-spelled-correctly.md)|A resource string contains one or more words that are not recognized by the Microsoft spelling checker library.|  
|[CA1724: Type Names Should Not Match Namespaces](../code-quality/ca1724--type-names-should-not-match-namespaces.md)|Type names should not match the names of namespaces that are defined in the [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] class library. Violation of this rule can reduce the usability of the library.|  
|[CA1707: Identifiers should not contain underscores](../code-quality/ca1707--identifiers-should-not-contain-underscores.md)|By convention, identifier names do not contain the underscore (_) character. This rule checks namespaces, types, members, and parameters.|  
|[CA1721: Property names should not match get methods](../code-quality/ca1721--property-names-should-not-match-get-methods.md)|The name of a public or protected member starts with "Get" and otherwise matches the name of a public or protected property. "Get" methods and properties should have names that clearly distinguish their function.|  
|[CA1716: Identifiers should not match keywords](../code-quality/ca1716--identifiers-should-not-match-keywords.md)|A namespace name or a type name matches a reserved keyword in a programming language. Identifiers for namespaces and types should not match keywords that are defined by languages that target the common language runtime.|  
|[CA1726: Use preferred terms](../code-quality/ca1726--use-preferred-terms.md)|The name of an externally visible identifier includes a term for which an alternative, preferred term exists. Alternatively, the name includes the term "Flag" or "Flags".|  
|[CA1709: Identifiers should be cased correctly](../code-quality/ca1709--identifiers-should-be-cased-correctly.md)|By convention, parameter names use camel casing, and namespace, type, and member names use Pascal casing.|  
|[CA1702: Compound words should be cased correctly](../code-quality/ca1702--compound-words-should-be-cased-correctly.md)|The name of an identifier contains multiple words, and at least one of the words appears to be a compound word that is not cased correctly.|  
|[CA1712: Do not prefix enum values with type name](../code-quality/ca1712--do-not-prefix-enum-values-with-type-name.md)|Names of enumeration members are not prefixed with the type name because type information is expected to be provided by development tools.|  
|[CA1710: Identifiers should have correct suffix](../code-quality/ca1710--identifiers-should-have-correct-suffix.md)|By convention, the names of types that extend certain base types or that implement certain interfaces, or types derived from these types, have a suffix that is associated with the base type or interface.|