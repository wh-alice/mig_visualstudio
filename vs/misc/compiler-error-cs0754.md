---
title: "Compiler Error CS0754"
ms.custom: ""
ms.date: "10/25/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0754"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0754"
ms.assetid: c83e04b5-6ab5-45c2-805e-0ba4f041d506
caps.latest.revision: 5
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
# Compiler Error CS0754
A partial method may not explicitly implement an interface method.  
  
 A partial method cannot be declared as an explicit implementation of a method defined in an interface.  
  
### To correct this error  
  
1.  Remove the explicit interface qualification from the method declaration.  
  
## Example  
 The following code generates CS0754:  
  
```  
// cs0754.cs  
using System;  
  
    public interface IF  
    {  
        void Part();  
    }  
  
    public partial class C : IF  
    {  
        partial void IF.Part(); //CS0754  
        public static int Main()  
        {  
            return 1;  
        }  
    }  
```  
  
## See Also  
 [Explicit Interface Implementation](../Topic/Explicit%20Interface%20Implementation%20\(C%23%20Programming%20Guide\).md)   
 [Partial Classes and Methods](../Topic/Partial%20Classes%20and%20Methods%20\(C%23%20Programming%20Guide\).md)