---
title: "Compiler Error CS0716 | Microsoft Docs"
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
  - "CS0716"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0716"
ms.assetid: 806d25ef-f8a7-4c94-823e-e07904defcf4
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
# Compiler Error CS0716
Cannot convert to static type 'type'  
  
 This error occurs if your code uses a cast to convert to a static type. Since it is not possible for an object to be an instance of a static type, casting to a static type can never be a meaningful cast.  
  
## Example  
 The following sample generates CS0716:  
  
```  
// CS0716.cs  
  
public static class SC  
{  
    static void F() { }  
}  
  
public class Test  
{  
    public static void Main()  
    {  
        object o = new object();  
        System.Console.WriteLine((SC)o);  // CS0716  
    }  
}  
```