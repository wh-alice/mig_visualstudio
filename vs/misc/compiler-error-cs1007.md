---
title: "Compiler Error CS1007 | Microsoft Docs"
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
  - "CS1007"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1007"
ms.assetid: b56ee2c6-8e79-4b9b-8c59-194bdb22bc3e
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
# Compiler Error CS1007
Property accessor already defined  
  
 When you declare a [property](/dotnet/csharp/programming-guide/classes-and-structs/using-properties), you must also declare its accessor methods. However, a property cannot have more than one `get` accessor method or more than one `set` accessor method.  
  
## Example  
 The following sample generates CS1007:  
  
```  
// CS1007.cs  
public class clx  
{  
    public int MyProperty  
    {  
        get  
        {  
            return 0;  
        }  
        get   // CS1007, this is the second get method  
        {  
            return 0;  
        }  
    }  
  
    public static void Main() {}  
}  
```