---
title: "Compiler Error CS0503 | Microsoft Docs"
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
  - "CS0503"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0503"
ms.assetid: 12a337c9-8c5d-473d-8ce6-057b2c7e7935
caps.latest.revision: 7
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
# Compiler Error CS0503
The abstract method 'method' cannot be marked virtual  
  
 It is redundant to mark a member method as both [abstract](/dotnet/csharp/language-reference/keywords/abstract) and [virtual](/dotnet/csharp/language-reference/keywords/virtual) because **abstract** implies **virtual**.  
  
 The following sample generates CS0503:  
  
```  
// CS0503.cs  
namespace x  
{  
   abstract public class clx  
   {  
      abstract virtual public void f();   // CS0503  
   }  
}  
```