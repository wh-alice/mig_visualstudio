---
title: "Compiler Error CS0757"
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
  - "CS0757"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0757"
ms.assetid: ba093570-306d-4b7b-aad5-1a3855ad6776
caps.latest.revision: 5
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
# Compiler Error CS0757
A partial method may not have multiple implementing declarations.  
  
 A partial method consists of exactly one defining declaration (signature) and one or zero implementing declarations (body). Multiple implementing declarations for the same identical defining declarations are not allowed. Partial methods may be overloaded, and each overloaded version may have one or zero implementing declarations.  
  
### To correct this error  
  
1.  Remove all except one of the implementing declarations for the partial method.  
  
## Example  
 The following example generates CS0757:  
  
```  
// cs0757.cs  
using System;  
  
    public partial class C  
    {  
        // Defining declaration.  
        partial void Part();  
  
        // Implementing declaration.  
        partial void Part()  
        {  
            //...Do something.  
        }  
  
        // Second implementing declaration.  
        partial void Part() // CS0757  
        {  
            //...Do something.  
        }  
  
        public static int Main()  
        {  
            return 1;  
        }  
    }  
```  
  
## See Also  
 [Partial Classes and Methods](../Topic/Partial%20Classes%20and%20Methods%20\(C%23%20Programming%20Guide\).md)