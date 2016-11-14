---
title: "Extension methods can be defined only in modules | Microsoft Docs"
ms.custom: ""
ms.date: "2015-07-20"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc36551"
  - "bc36551"
helpviewer_keywords: 
  - "BC36551"
ms.assetid: c832d523-5bf6-4baf-b91c-bd26d94453ed
caps.latest.revision: 22
author: "stevehoag"
ms.author: "shoag"
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
 [Extension Methods](/dotnet/visual-basic/language-reference/procedures/extension-methods)   
 [Module \<keyword>](http://msdn.microsoft.com/en-us/Library/d971b940-05ab-4d56-8485-e3b8a661906b)   
 [Module Statement](/dotnet/visual-basic/language-reference/statements/module-statement)