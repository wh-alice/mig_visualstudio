---
title: "Compiler Error CS0550"
ms.custom: ""
ms.date: "10/25/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0550"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0550"
ms.assetid: 57278c17-443c-40f2-9ebd-853558743564
caps.latest.revision: 9
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
# Compiler Error CS0550
'accessor' adds an accessor not found in interface member 'property'  
  
 The implementation of a property in a derived class contains an accessor that was not specified in the base interface.  
  
 For more information, see [Using Properties](../Topic/Using%20Properties%20\(C%23%20Programming%20Guide\).md).  
  
## Example  
 The following sample generates CS0550.  
  
```  
// CS0550.cs  
namespace x  
{  
   interface ii  
   {  
      int i  
      {  
         get;  
         // add the following accessor to resolve this CS0550  
         // set;  
      }  
   }  
  
   public class a : ii  
   {  
      int ii.i  
      {  
         get  
         {  
            return 0;  
         }  
         set {}   // CS0550  no set in interface  
      }  
  
      public static void Main() {}  
   }  
}  
```