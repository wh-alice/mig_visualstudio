---
title: "Compiler Error CS0547 | Microsoft Docs"
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
  - "CS0547"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0547"
ms.assetid: aa80873f-deb0-4ff2-8435-92a626bb5b80
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
# Compiler Error CS0547
'property' : property or indexer cannot have void type  
  
 [void](/dotnet/csharp/language-reference/keywords/void) is invalid as a return value for a property.  
  
 For more information, see [Properties](/dotnet/csharp/programming-guide/classes-and-structs/properties).  
  
 The following sample generates CS0547:  
  
```  
// CS0547.cs  
public class a  
{  
   public void i   // CS0547  
   // Try the following declaration instead:  
   // public int i  
   {  
      get  
      {  
         return 0;  
      }  
   }  
}  
  
public class b : a  
{  
   public static void Main()  
   {  
   }  
}  
```