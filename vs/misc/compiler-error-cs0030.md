---
title: "Compiler Error CS0030"
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
  - "CS0030"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0030"
ms.assetid: 3c9bd3f9-dea2-46dd-be1e-46c843ffd3de
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
# Compiler Error CS0030
Cannot convert type 'type' to 'type'  
  
 You must provide conversion routines to support certain operator overloads. For more information, see [Conversion Operators](../Topic/Conversion%20Operators%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0030:  
  
```  
// CS0030.cs  
namespace x  
{  
   public class iii  
   {  
      /*  
      public static implicit operator iii(int aa)  
      {  
         return null;  
      }  
  
      public static implicit operator int(iii aa)  
      {  
         return 0;  
      }  
      */  
  
      public static iii operator ++(iii aa)  
      {  
         return (iii)0;   // CS0030  
         // uncomment the conversion routines to resolve CS0030  
      }  
  
      public static void Main()  
      {  
      }  
   }  
}  
```