---
title: "Extension methods can be defined only in modules | testtitle"
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
  - "vbc36551"
  - "bc36551"
helpviewer_keywords: 
  - "BC36551"
ms.assetid: c832d523-5bf6-4baf-b91c-bd26d94453ed
caps.latest.revision: 22
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
# Extension methods can be defined only in modules
This error occurs when an extension method has been defined outside a module. In Visual Basic, all extension methods must be defined within standard modules.  
  
 **Error ID:** BC36551  
  
### To correct this error  
  
-   Place the extension method in a module.  
  
## Example  
 The following example extends the `String` class, adding a `Print` method.  
  
```  
Imports StringUtility  
Imports System.Runtime.CompilerServices  
Namespace StringUtility  
    <Extension()> _  
    Module StringExtensions  
        <Extension()> _  
        Public Sub Print (ByVal str As String)  
            Console.WriteLine(str)  
        End Sub  
    End Module  
End Namespace  
```  
  
## See Also  
 [NOT IN BUILD: Application of Attributes](http://msdn.microsoft.com/en-us/2b1703ed-4437-49b3-bc0b-568094324f47)   
 [Extension Methods](../Topic/Extension%20Methods%20\(Visual%20Basic\).md)   
 [Module \<keyword>](../Topic/Module%20%3Ckeyword%3E%20\(Visual%20Basic\).md)   
 [Module Statement](../Topic/Module%20Statement.md)