---
title: "Compiler Error CS0158 | Microsoft Docs"
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
  - "CS0158"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0158"
ms.assetid: 88ac61a9-ce55-4272-9141-0873765a7034
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
# Compiler Error CS0158
The label 'label' shadows another label by the same name in a contained scope  
  
 A label in an inner scope hides a label with the same name in an outer scope. For more information, see [goto](/dotnet/csharp/language-reference/keywords/goto).  
  
 The following sample generates CS0158:  
  
```  
// CS0158.cs  
namespace MyNamespace  
{  
   public class MyClass  
   {  
      public static void Main()  
      {  
         goto lab1;  
         lab1:  
         {  
            lab1:  
            goto lab1;   // CS0158  
         }  
      }  
   }  
}  
```