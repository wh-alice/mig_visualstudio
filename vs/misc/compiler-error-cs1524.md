---
title: "Compiler Error CS1524"
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
  - "CS1524"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1524"
ms.assetid: a7b80bbc-a2de-4718-b0f0-4c9526726525
caps.latest.revision: 8
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
# Compiler Error CS1524
Expected catch or finally  
  
 A `try` block must be followed by a `catch` or `finally` block.  
  
 For more information on exceptions, see [Exception Handling Statements](../Topic/Exception%20Handling%20Statements%20\(C%23%20Reference\).md).  
  
## Example  
 The following sample generates CS1524:  
  
```  
// CS1524.cs  
class x  
{  
    public static void Main()  
    {  
        try  
        {  
            // Code here  
        }  
        catch  
        {  
        }  
        try  
        {  
            // Code here  
        }  
        finally  
        {  
        }  
        try  
        {  
            // Code here  
        }  
    }     // CS1524, missing catch or finally  
}  
```