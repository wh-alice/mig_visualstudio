---
title: "Compiler Error CS1913 | Microsoft Docs"
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
  - "CS1913"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1913"
ms.assetid: 652494b3-9576-4a4c-a9ee-695f86c4a023
caps.latest.revision: 7
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
# Compiler Error CS1913
Member 'name' cannot be initialized. It is not a field or property.  
  
 Object initializers can only be used to initialize accessible fields or properties.  
  
### To correct this error  
  
1.  Initialize the class member in a regular constructor or other initialization method.  
  
## Example  
 The following example generates CS1913:  
  
```  
// cs1912.cs  
class A  
{  
    public delegate void D();  
    public event D myEvent;  
}  
  
public class Test  
{  
    static void Main()  
    {  
  
        A a = new A() {myEvent = M}; // CS1913  
    }  
  
    public void M(){}  
}  
```  
  
## See Also  
 [Classes and Structs](../Topic/Classes%20and%20Structs%20\(C%23%20Programming%20Guide\).md)