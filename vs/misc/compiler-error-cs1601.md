---
title: "Compiler Error CS1601 | Microsoft Docs"
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
  - "CS1601"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1601"
ms.assetid: 5efa1d2d-c70c-446d-a51f-d23d8a3be22e
caps.latest.revision: 10
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
# Compiler Error CS1601
Method or delegate parameter cannot be of type 'type'  
  
 Some types in the .NET Framework class library, for example, <xref:System.TypedReference>, <xref:System.RuntimeArgumentHandle> and <xref:System.ArgIterator> cannot be used as [ref](/dotnet/csharp/language-reference/keywords/ref) or [out](/dotnet/csharp/language-reference/keywords/out) parameters because they could potentially be used to perform unsafe operations.  
  
 The following sample generates CS1601:  
  
```  
// CS1601.cs  
using System;  
  
class MyClass  
{  
   public void Test1 (ref TypedReference t)   // CS1601  
   {  
   }  
  
   public void Test2 (out ArgIterator t)   // CS1601  
   {  
   }  
}  
```