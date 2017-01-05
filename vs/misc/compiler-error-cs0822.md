---
title: "Compiler Error CS0822"
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
  - "CS0822"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0822"
ms.assetid: 519091be-2332-4df4-acd9-e3b633966b3d
caps.latest.revision: 7
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
# Compiler Error CS0822
Implicitly typed locals cannot be const  
  
 Implicitly typed local variables are only necessary for storing anonymous types. In all other cases they are just a convenience. If the value of the variable never changes, just give it an explicit type. Attempting to use the `readonly` modifier with an implicitly typed local will generate CS0106.  
  
### To correct this error  
  
1.  If you require the variable to be constant or `readonly`, give it an explicit type.  
  
## Example  
 The following code generates CS0822:  
  
```  
// cs0822.cs  
class A  
{  
  
    public static int Main()  
    {  
        const var x = 0; // CS0822.cs  
        return -1;  
    }  
}  
```  
  
## See Also  
 [Implicitly Typed Local Variables](../Topic/Implicitly%20Typed%20Local%20Variables%20\(C%23%20Programming%20Guide\).md)