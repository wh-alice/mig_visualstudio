---
title: "Compiler Error CS1912"
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
  - "CS1912"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1912"
ms.assetid: 6205420e-01b9-4470-89f9-5924f1e49108
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
# Compiler Error CS1912
Duplicate initialization of member 'name'.  
  
 An object initializer can initialize each member only one time.  
  
### To correct this error  
  
1.  Remove the second initialization of the member in the object initializer.  
  
## Example  
 The following code generates CS1912 because `memberA` is initialized two times:  
  
```  
// cs1912.cs  
using System.Linq;  
  
public class TestClass  
{  
    public int memberA { get; set; }  
    public int memberB { get; set; }  
}  
  
public class Test  
{  
    static void Main()  
    {  
        TestClass tc = new TestClass() { memberA = 5, memberA = 6, memberB = 2}; // CS1912  
    }  
}  
```  
  
## See Also  
 [Object and Collection Initializers](../Topic/Object%20and%20Collection%20Initializers%20\(C%23%20Programming%20Guide\).md)