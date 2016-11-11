---
title: "Compiler Error CS1530 | Microsoft Docs"
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
  - "CS1530"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1530"
ms.assetid: 3844b5ef-e0ec-42df-9267-72689020f128
caps.latest.revision: 8
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
# Compiler Error CS1530
Keyword 'new' is not allowed on elements defined in a namespace  
  
 It is not necessary to specify the [new](/dotnet/csharp/language-reference/keywords/new) keyword on any construct that is in a [namespace](/dotnet/csharp/language-reference/keywords/namespace).  
  
 The following sample generates CS1530:  
  
```  
// CS1530.cs  
namespace a  
{  
   new class i   // CS1530  
   {  
   }  
  
   // try the following instead  
   class ii  
   {  
      public static void Main()  
      {  
      }  
   }  
}  
```