---
title: "Compiler Error CS1055 | Microsoft Docs"
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
  - "CS1055"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1055"
ms.assetid: a93cb577-95fc-490a-97c4-2f366409f2c3
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
# Compiler Error CS1055
An add or remove accessor expected  
  
 If your [event](/dotnet/csharp/language-reference/keywords/event) is not declared as a field, it must define both **add** and **remove** accessor functions.  
  
 The following sample generates CS1055:  
  
```  
// CS1055.cs  
delegate void del();  
class Test  
{  
   public event del MyEvent  
   {  
      int i;   // CS1055  
      // uncomment accessors and delete previous line to resolve  
      // add  
      // {  
      //    MyEvent += value;  
      // }  
      // remove  
      // {  
      //    MyEvent -= value;  
      // }  
   }  
  
   public static void Main()  
   {  
   }  
}  
```