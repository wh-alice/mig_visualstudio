---
title: "Compiler Warning (level 4) CS0628 | Microsoft Docs"
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
  - "CS0628"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0628"
ms.assetid: a54cfad8-27c9-4abb-8c83-982615489a10
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
# Compiler Warning (level 4) CS0628
'member' : new protected member declared in sealed class  
  
 A [sealed](/dotnet/csharp/language-reference/keywords/sealed) class cannot introduce a [protected](/dotnet/csharp/language-reference/keywords/protected) member because no other class will be able to inherit from the `sealed` class and use the `protected` member.  
  
 The following sample generates CS0628:  
  
```  
// CS0628.cs  
// compile with: /W:4  
sealed class C  
{  
   protected int i;   // CS0628  
}  
  
class MyClass  
{  
   public static void Main()  
   {  
   }  
}  
```