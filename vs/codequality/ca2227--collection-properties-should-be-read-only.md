---
title: "CA2227: Collection properties should be read only"
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
  - "CA2227"
  - "CollectionPropertiesShouldBeReadOnly"
helpviewer_keywords: 
  - "CA2227"
  - "CollectionPropertiesShouldBeReadOnly"
ms.assetid: 26967aaf-6fbe-438a-b4d3-ac579b5dc0f9
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
# CA2227: Collection properties should be read only
|||  
|-|-|  
|TypeName|CollectionPropertiesShouldBeReadOnly|  
|CheckId|CA2227|  
|Category|Microsoft.Usage|  
|Breaking Change|Breaking|  
  
## Cause  
 An externally visible writable property is a type that implements \<xref:System.Collections.ICollection?displayProperty=fullName>. Arrays, indexers (properties with the name 'Item'), and permission sets are ignored by the rule.  
  
## Rule Description  
 A writable collection property allows a user to replace the collection with a completely different collection. A read-only property stops the collection from being replaced but still allows the individual members to be set. If replacing the collection is a goal, the preferred design pattern is to include a method to remove all the elements from the collection and a method to re-populate the collection. See the \<xref:System.Collections.ArrayList.Clear*> and \<xref:System.Collections.ArrayList.AddRange*> methods of the \<xref:System.Collections.ArrayList?displayProperty=fullName> class for an example of this pattern.  
  
 Both binary and XML serialization support read-only properties that are collections. The \<xref:System.Xml.Serialization.XmlSerializer?displayProperty=fullName> class has specific requirements for types that implement \<xref:System.Collections.ICollection> and \<xref:System.Collections.IEnumerable?displayProperty=fullName> in order to be serializable.  
  
## How to Fix Violations  
 To fix a violation of this rule, make the property read-only and, if the design requires it, add methods to clear and re-populate the collection.  
  
## When to Suppress Warnings  
 Do not suppress a warning from this rule.  
  
## Example  
 The following example shows a type with a writable collection property and shows how the collection can be replaced directly. Additionally, the preferred manner of replacing a read-only collection property using `Clear` and `AddRange` methods is shown.  
  
 [!code[FxCop.Usage.PropertiesReturningCollections#1](../codequality/codesnippet/CSharp/ca2227--collection-properties-should-be-read-only_1.cs)]
[!code[FxCop.Usage.PropertiesReturningCollections#1](../codequality/codesnippet/VisualBasic/ca2227--collection-properties-should-be-read-only_1.vb)]
[!code[FxCop.Usage.PropertiesReturningCollections#1](../codequality/codesnippet/CPP/ca2227--collection-properties-should-be-read-only_1.cpp)]  
  
## Related Rules  
 [CA1819: Properties should not return arrays](../codequality/ca1819--properties-should-not-return-arrays.md)