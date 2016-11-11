---
title: "Compiler Error CS0023 | Microsoft Docs"
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
  - "CS0023"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0023"
ms.assetid: 7a30073c-99de-41fa-ac6d-4a0dfbb76de9
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
# Compiler Error CS0023
Operator 'operator' cannot be applied to operand of type 'type'  
  
 An attempt was made to apply an operator to a variable whose type was not designed to work with the operator. For more information, see [Types](/dotnet/csharp/programming-guide/types/index) and [C# Operators](/dotnet/csharp/language-reference/operators/index).  
  
 The following sample generates CS0023:  
  
```  
// CS0023.cs  
namespace x  
{  
   public class a  
   {  
      public static void Main()  
      {  
         string s = "hello";  
         s = -s;   // CS0023, minus operator not allowed on strings  
      }  
   }  
}  
```