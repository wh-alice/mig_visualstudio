---
title: "Compiler Error CS1618 | Microsoft Docs"
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
  - "CS1618"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1618"
ms.assetid: e046d402-208e-48fd-8ff3-bb03044036c4
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
# Compiler Error CS1618
Cannot create delegate with 'method' because it has a Conditional attribute  
  
 You cannot create a delegate with a conditional method because the method might not exist in some builds.  
  
 The following sample generates CS1618:  
  
```  
// CS1618.cs  
using System;  
using System.Diagnostics;  
  
delegate void del();  
  
class MakeAnError {  
   public static void Main() {  
      del d = new del(ConditionalMethod);   // CS1618  
      // Invalid because on builds where DEBUG is not set,   
      // there will be no "ConditionalMethod".  
   }  
   // To fix the error, remove the next line:  
   [Conditional("DEBUG")]  
   public static void ConditionalMethod()   
   {  
      Console.WriteLine("Do something only in debug");  
   }  
}  
```