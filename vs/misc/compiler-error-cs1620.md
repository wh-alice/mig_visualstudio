---
title: "Compiler Error CS1620"
ms.custom: ""
ms.date: "10/19/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS1620"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1620"
ms.assetid: 13933976-218a-4fe2-8fde-5b9af522e2e5
caps.latest.revision: 8
ms.author: "billchi"
manager: "douge"
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
# Compiler Error CS1620
Argument 'number' must be passed with the 'keyword' keyword  
  
 This error occurs if you are passing an argument to a function that takes a [ref](../Topic/ref%20\(C%23%20Reference\).md) or [out](../Topic/out%20\(C%23%20Reference\).md) parameter and you don't include the `ref` or `out` keyword at the point of call, or you include the wrong keyword. The error text indicates the appropriate keyword to use and which argument caused the failure.  
  
 The following sample generates CS1620:  
  
```  
// CS1620.cs  
class C  
{  
    void f(ref int i) {}  
    public static void Main()  
    {  
        int x = 1;  
        f(out x);  // CS1620 – f takes a ref parameter, not an out parameter  
        // Try this line instead:  
        // f(ref x);  
    }  
}  
```