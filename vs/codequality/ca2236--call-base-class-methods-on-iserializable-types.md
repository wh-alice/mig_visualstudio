---
title: "CA2236: Call base class methods on ISerializable types"
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
  - "CA2236"
  - "CallBaseClassMethodsOnISerializableTypes"
helpviewer_keywords: 
  - "CA2236"
  - "CallBaseClassMethodsOnISerializableTypes"
ms.assetid: 5a15b20d-769c-4640-b31a-36e07077daae
caps.latest.revision: 15
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
# CA2236: Call base class methods on ISerializable types
|||  
|-|-|  
|TypeName|CallBaseClassMethodsOnISerializableTypes|  
|CheckId|CA2236|  
|Category|Microsoft.Usage|  
|Breaking Change|Non Breaking|  
  
## Cause  
 A type derives from a type that implements the \<xref:System.Runtime.Serialization.ISerializable?displayProperty=fullName> interface, and one of the following conditions is true:  
  
-   The type implements the serialization constructor, that is, a constructor with the \<xref:System.Runtime.Serialization.SerializationInfo?displayProperty=fullName>, \<xref:System.Runtime.Serialization.StreamingContext?displayProperty=fullName> parameter signature, but does not call the serialization constructor of the base type.  
  
-   The type implements the \<xref:System.Runtime.Serialization.ISerializable.GetObjectData*?displayProperty=fullName> method but does not call the \<xref:System.Runtime.Serialization.ISerializable.GetObjectData*> method of the base type.  
  
## Rule Description  
 In a custom serialization process, a type implements the \<xref:System.Runtime.Serialization.ISerializable.GetObjectData*> method to serialize its fields and the serialization constructor to de-serialize the fields. If the type derives from a type that implements the \<xref:System.Runtime.Serialization.ISerializable> interface, the base type \<xref:System.Runtime.Serialization.ISerializable.GetObjectData*> method and serialization constructor should be called to serialize/de-serialize the fields of the base type. Otherwise, the type will not be serialized and de-serialized correctly. Note that if the derived type does not add any new fields, the type does not need to implement the \<xref:System.Runtime.Serialization.ISerializable.GetObjectData*> method nor the serialization constructor or call the base type equivalents.  
  
## How to Fix Violations  
 To fix a violation of this rule, call the base type \<xref:System.Runtime.Serialization.ISerializable.GetObjectData*> method or serialization constructor from the corresponding derived type method or constructor.  
  
## When to Suppress Warnings  
 Do not suppress a warning from this rule.  
  
## Example  
 The following example shows a derived type that satisfies the rule by calling the serialization constructor and \<xref:System.Runtime.Serialization.ISerializable.GetObjectData*> method of the base class.  
  
 [!code[FxCop.Usage.CallBaseISerializable#1](../codequality/codesnippet/VisualBasic/ca2236--call-base-class-methods-on-iserializable-types_1.vb)]
[!code[FxCop.Usage.CallBaseISerializable#1](../codequality/codesnippet/CSharp/ca2236--call-base-class-methods-on-iserializable-types_1.cs)]  
  
## Related Rules  
 [CA2240: Implement ISerializable correctly](../codequality/ca2240--implement-iserializable-correctly.md)  
  
 [CA2229: Implement serialization constructors](../codequality/ca2229--implement-serialization-constructors.md)  
  
 [CA2238: Implement serialization methods correctly](../codequality/ca2238--implement-serialization-methods-correctly.md)  
  
 [CA2235: Mark all non-serializable fields](../codequality/ca2235--mark-all-non-serializable-fields.md)  
  
 [CA2237: Mark ISerializable types with SerializableAttribute](../codequality/ca2237--mark-iserializable-types-with-serializableattribute.md)  
  
 [CA2239: Provide deserialization methods for optional fields](../codequality/ca2239--provide-deserialization-methods-for-optional-fields.md)  
  
 [CA2120: Secure serialization constructors](../codequality/ca2120--secure-serialization-constructors.md)