---
title: "Compiler Error CS0196 | Microsoft Docs"
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
  - "CS0196"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0196"
ms.assetid: d361484e-73b8-439a-99c7-714e61d73755
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
# Compiler Error CS0196
A pointer must be indexed by only one value  
  
 A pointer cannot have multiple indices. For more information, see [Pointer types](/dotnet/csharp/programming-guide/unsafe-code-pointers/pointer-types)  
  
 The following sample generates CS0196:  
  
```  
// CS0196.cs  
public class MyClass  
{  
   public static void Main ()  
   {  
      int *i = null;  
      int j = 0;  
      j = i[1,2];   // CS0196  
      // try the following line instead  
      // j = i[1];  
   }  
}  
```