---
title: "Compiler Error CS1689"
ms.custom: na
ms.date: "10/01/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "CS1689"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1689"
ms.assetid: 5fa6e845-40ef-4451-81ee-acbe2665527a
caps.latest.revision: 10
ms.author: "billchi"
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
# Compiler Error CS1689
Attribute 'Attribute Name' is only valid on methods or attribute classes  
  
 This error only occurs with the **ConditionalAttribute** attribute. As the message states, this attribute can only be used on methods or attribute classes. For example, trying to apply this attribute to a class will generate this error.  
  
## Example  
 The following sample generates CS1689.  
  
```  
// CS1689.cs  
// compile with: /target:library  
[System.Diagnostics.Conditional("A")]   // CS1689  
class MyClass {}  
```