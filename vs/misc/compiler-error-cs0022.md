---
title: "Compiler Error CS0022 | Microsoft Docs"
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
  - "CS0022"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0022"
ms.assetid: 531c3ed2-0d75-4046-8d57-89f79381af8e
caps.latest.revision: 8
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
# Compiler Error CS0022
Wrong number of indices inside [], expected 'number'  
  
 An array-access operation specified the incorrect number of dimensions within the square brackets. For more information, see [Arrays](/dotnet/csharp/programming-guide/arrays/index).  
  
## Example  
 The following sample generates CS0022:  
  
```  
// CS0022.cs  
public class MyClass  
{  
    public static void Main()  
    {  
        int[] a = new int[10];  
        a[0] = 0;     // single-dimension array  
        a[0,1] = 9;   // CS0022, the array does not have two dimensions  
    }  
}  
```