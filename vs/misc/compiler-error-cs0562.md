---
title: "Compiler Error CS0562"
ms.custom: ""
ms.date: "10/13/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0562"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0562"
ms.assetid: dceecce5-90ce-4554-820c-f4c06b2b8258
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
# Compiler Error CS0562
The parameter of a unary operator must be the containing type  
  
 The method declaration for an operator overload must follow certain guidelines. For more information, see [Overloadable Operators](../Topic/Overloadable%20Operators%20\(C%23%20Programming%20Guide\).md) and [Operator Overloading Sample](http://msdn.microsoft.com/en-us/1c6b4610-0a49-4532-8fa7-f694cfc65743).  
  
## Example  
 The following sample generates CS0562:  
  
```  
// CS0562.cs  
public class iii  
{  
    public static implicit operator int(iii x)  
    {  
        return 0;  
    }  
  
    public static implicit operator iii(int x)  
    {  
        return null;  
    }  
  
    public static iii operator +(int aa)   // CS0562  
    // try the following line instead  
    // public static iii operator +(iii aa)  
    {  
        return (iii)0;  
    }  
  
    public static void Main()  
    {  
    }  
}  
```