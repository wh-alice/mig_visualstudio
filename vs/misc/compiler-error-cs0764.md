---
title: "Compiler Error CS0764 | hehe"
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
  - "CS0764"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0764"
ms.assetid: 76a64149-49d8-40ea-a976-03835d8fb7eb
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
# Compiler Error CS0764
Both partial method declarations must be unsafe or neither may be unsafe  
  
 A partial method consists of a defining declaration (signature) and an optional implementing declaration (body). If the defining declaration has the `unsafe` modifier, the implementing declaration must also have it. Conversely, if the implementing declaration has the `unsafe` modifier, the defining declaration must also.  
  
### To correct this error  
  
1.  Assuming that the defining declaration is correct, add or remove the `unsafe` modifier from the implementing declaration to match the defining declaration.  
  
## Example  
  
```  
// cs0764.cs  
//  Compile with: /target:library /unsafe  
public partial class C  
{  
    partial void Part();  
    unsafe partial void Part() //CS0764  
    {  
    }  
  
    public static int Main()  
    {  
        return 1;  
    }  
}  
```  
  
## See Also  
 [Partial Classes and Methods](../Topic/Partial%20Classes%20and%20Methods%20\(C%23%20Programming%20Guide\).md)