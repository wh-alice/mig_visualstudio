---
title: "Compiler Error CS1551"
ms.custom: na
ms.date: "10/02/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "CS1551"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1551"
ms.assetid: 09fde2a2-7466-418a-88ef-395321358b07
caps.latest.revision: 7
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
# Compiler Error CS1551
Indexers must have at least one parameter  
  
 An [indexer](../Topic/Indexers%20\(C%23%20Programming%20Guide\).md) that takes no arguments was declared.  
  
 The following sample generates CS1551:  
  
```  
// CS1551.cs  
public class MyClass  
{  
   int intI;  
  
   int this[]   // CS1551  
   // try the following line instead  
   // int this[int i]  
   {  
      get  
      {  
         return intI;  
      }  
      set  
      {  
         intI = value;  
      }  
   }  
  
   public static void Main()  
   {  
   }  
}  
```