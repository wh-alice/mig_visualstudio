---
title: "Compiler Error CS1663 | Microsoft Docs"
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
  - "CS1663"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1663"
ms.assetid: 013f36ac-8925-4cee-9008-54fa7ad1324b
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
# Compiler Error CS1663
Fixed size buffer type must be one of the following: bool, byte, short, int, long, char, sbyte, ushort, uint, ulong, float or double  
  
 A fixed sized buffer may not be any type other than those listed. To avoid this error, use another type or do not use a fixed array.  
  
## Example  
 The following sample generates CS1663.  
  
```  
// CS1663.cs  
// compile with: /unsafe /target:library  
  
unsafe struct C  
{  
   fixed string ab[10];   // CS1663  
}  
```