---
title: "Compiler Error CS0466 | Microsoft Docs"
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
  - "CS0466"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0466"
ms.assetid: db6be72b-120a-4b48-b41c-a738d02adae0
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
# Compiler Error CS0466
'method1' should not have a params parameter since 'method2' does not  
  
 You cannot use `params` parameter on a class member if the implemented interface doesn't use it.  
  
## Example  
 The following sample generates CS0466.  
  
```  
// CS0466.cs  
interface I  
{  
   void F1(params int[] a);  
   void F2(int[] a);  
}  
  
class C : I  
{  
   void I.F1(params int[] a) {}  
   void I.F2(params int[] a) {}   // CS0466  
   void I.F2(int[] a) {}   // OK  
  
   public static void Main()  
   {  
      I i = (I) new C();  
  
      i.F1(new int[] {1, 2} );  
      i.F2(new int[] {1, 2} );  
   }  
}  
```