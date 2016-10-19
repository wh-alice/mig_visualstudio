---
title: "Compiler Error CS0825"
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
  - "CS0825"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0825"
ms.assetid: 49393d23-ec5f-4b44-a3fd-7e0a95ac0edd
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
# Compiler Error CS0825
The contextual keyword 'var' may only appear within a local variable declaration.  
  
 Implicit typing with the `var` keyword can only be applied to variables at local method scope.  
  
### To correct this error  
  
1.  If the variable belongs at class scope, give it an explicit type.  Otherwise move it inside the method where it will be used.  
  
## Example  
 The following code generates CS0825 because `var` is used on a class field:  
  
```  
// cs0825.cs  
class Test  
{  
    private var myField; //CS0825  
  
    static int Main()  
    {  
        var a = 1; // var is OK here  
        return -1;  
    }  
}  
```  
  
## See Also  
 [Implicitly Typed Local Variables](../Topic/Implicitly%20Typed%20Local%20Variables%20\(C%23%20Programming%20Guide\).md)