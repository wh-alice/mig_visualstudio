---
title: "Compiler Error CS1628 | Microsoft Docs"
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
  - "CS1628"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1628"
ms.assetid: 520f864c-afe3-4db2-b44e-cfaac28ff49d
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
# Compiler Error CS1628
Cannot use ref or out parameter 'parameter' inside an anonymous method, lambda expression, or query expression  
  
 This error occurs if you use a ref or out parameter inside an anonymous method block. To avoid this error, use a local variable or some other construct.  
  
 The following sample generates CS1628:  
  
```  
// CS1628.cs  
  
delegate int MyDelegate();  
  
class C  
{  
  public static void F(ref int i)  
  {  
      MyDelegate d = delegate { return i; };  // CS1628  
      // Try this instead:  
      // int tmp = i;  
      // MyDelegate d = delegate { return tmp; };  
  }  
  
  public static void Main()  
  {  
  
  }  
}  
```