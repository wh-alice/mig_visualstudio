---
title: "Compiler Error CS1008 | Microsoft Docs"
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
  - "CS1008"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1008"
ms.assetid: e595a431-2cf0-4cc1-998f-94aecb2a6db1
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
# Compiler Error CS1008
Type byte, sbyte, short, ushort, int, uint, long, or ulong expected  
  
 Certain data types, such as [enums](/dotnet/csharp/language-reference/keywords/enum), can only be declared to hold data of specified types.  
  
 The following sample generates CS1008:  
  
```  
// CS1008.cs  
abstract public class clx  
{  
   enum splitch : char   // CS1008, char not valid type for enums  
   {  
      x, y, z  
   }  
  
   public static void Main()  
   {  
   }  
}  
```