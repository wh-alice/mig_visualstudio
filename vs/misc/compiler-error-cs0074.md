---
title: "Compiler Error CS0074 | Microsoft Docs"
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
  - "CS0074"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0074"
ms.assetid: 9395c532-3934-4553-8e41-042bfe3399ce
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
# Compiler Error CS0074
'event': abstract event cannot have initializer  
  
 If an [event](/dotnet/csharp/language-reference/keywords/event) is marked as **abstract**, it cannot be initialized. For more information, see [Events](/dotnet/csharp/programming-guide/events/index).  
  
 The following sample generates CS0074:  
  
```  
// CS0074.cs  
delegate void D();  
  
abstract class Test  
{  
   public abstract event D e = null;   // CS0074  
   // try the following line instead  
   // public abstract event D e;  
  
   public static void Main()  
   {  
   }  
}  
```