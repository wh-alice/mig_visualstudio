---
title: "Compiler Error CS1007"
ms.custom: na
ms.date: "10/01/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "CS1007"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1007"
ms.assetid: b56ee2c6-8e79-4b9b-8c59-194bdb22bc3e
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
# Compiler Error CS1007
Property accessor already defined  
  
 When you declare a [property](../Topic/Using%20Properties%20\(C%23%20Programming%20Guide\).md), you must also declare its accessor methods. However, a property cannot have more than one `get` accessor method or more than one `set` accessor method.  
  
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