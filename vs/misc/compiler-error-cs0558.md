---
title: "Compiler Error CS0558"
ms.custom: ""
ms.date: "12/05/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0558"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0558"
ms.assetid: af63b9ba-2790-4362-a49d-b69a5292a555
caps.latest.revision: 7
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
# Compiler Error CS0558
User-defined operator 'operator' must be declared static and public  
  
 Both the **static** and **public** access [modifiers](../Topic/Modifiers%20\(C%23%20Reference\).md) must be specified on user-defined operators.  
  
 The following sample generates CS0558:  
  
```  
// CS0558.cs  
namespace x  
{  
   public class ii  
   {  
      public class iii  
      {  
         static implicit operator int(iii aa)   // CS0558, add public  
         {  
            return 0;  
         }  
      }  
  
      public static void Main()  
      {  
      }  
   }  
}  
```