---
title: "Compiler Error CS0833"
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
  - "CS0833"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0833"
ms.assetid: 4ae32454-265f-47aa-bf2a-ee1d702330b7
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
# Compiler Error CS0833
An anonymous type cannot have multiple properties with the same name.  
  
 An anonymous type, just like any type, cannot have two properties that have the same name.  
  
### To correct this error  
  
1.  Give each property in the type a unique name.  
  
## Example  
 The following example generates CS0833:  
  
```  
// cs0833.cs  
using System;  
  
public class C  
{  
    public static int Main()  
    {  
        var c = new { p1 = 1, p1 = 2 }; // CS0833  
        return 1;  
    }  
}  
```  
  
## See Also  
 [Anonymous Types](../Topic/Anonymous%20Types%20\(C%23%20Programming%20Guide\).md)