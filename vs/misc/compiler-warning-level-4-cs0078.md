---
title: "Compiler Warning (level 4) CS0078 | Microsoft Docs"
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
  - "CS0078"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0078"
ms.assetid: 8d637be6-82bc-462c-bec5-217327bc8c40
caps.latest.revision: 6
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
# Compiler Warning (level 4) CS0078
The 'l' suffix is easily confused with the digit '1' -- use 'L' for clarity  
  
 The compiler warns when it detects a cast to long using a lowercase l instead of an uppercase L.  
  
 The following sample generates CS0078:  
  
```  
// CS0078.cs  
// compile with: /W:4  
class test {  
   public static void TestL(long i)  
   {  
   }  
  
   public static void TestL(int i)  
   {  
   }  
  
   public static void Main()  
   {  
      TestL(25l);   // CS0078  
      // try the following line instead  
      // TestL(25L);  
   }  
}  
```