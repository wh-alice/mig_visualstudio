---
title: "Compiler Error CS1676 | Microsoft Docs"
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
  - "CS1676"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1676"
ms.assetid: 5ac83d98-5baa-49fd-b76a-d8ef0865b9dd
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
# Compiler Error CS1676
Parameter 'number' must be declared with the 'keyword' keyword  
  
 This error occurs when the parameter type modifier in an anonymous method is different from that used in the declaration of the delegate you are casting the method to.  
  
 The following sample generates CS1676:  
  
```  
// CS1676.cs  
delegate void E(ref int i);  
class Errors   
{  
   static void Main()  
   {  
      E e = delegate(out int i) { };   // CS1676  
      // To resolve, use the following line instead:  
      // E e = delegate(ref int i) { };  
   }  
}  
```