---
title: "Compiler Error CS0138 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0138"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0138"
ms.assetid: 970545f8-5ee5-428e-921a-3aa29f68d16d
caps.latest.revision: 9
author: "BillWagner"
ms.author: "wiwagn"
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
# Compiler Error CS0138
A using namespace directive can only be applied to namespaces; 'type' is a type not a namespace  
  
 A [using](/dotnet/csharp/language-reference/keywords/using) directive can only take the name of a namespace as a parameter. For more information, see [Namespaces](/dotnet/csharp/programming-guide/namespaces/index).  
  
 The following sample generates CS0138:  
  
```  
// CS0138.cs  
using System.Object;   // CS0138  
```