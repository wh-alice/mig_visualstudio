---
title: "Method arguments must be enclosed in parentheses | Microsoft Docs"
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
  - "vbc30800"
  - "bc30800"
helpviewer_keywords: 
  - "BC30800"
ms.assetid: ecdec760-8b51-474f-acad-17cf8059d83b
caps.latest.revision: 8
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
# Method arguments must be enclosed in parentheses
The rules governing procedure calls are simpler in newer versions of [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]. All arguments must be enclosed by parentheses.  
  
 **Error ID:** BC30800  
  
### To correct this error  
  
-   Enclose the argument list in parentheses; for example:  
  
    ```  
    MySub(ArrayIndex, NewValue)  
    ```  
  
## See Also  
 [Procedure Calling Sequence Changes in Visual Basic](http://msdn.microsoft.com/en-us/4ef1eea6-36cb-4b97-a31b-9ba65e46a9fd)   
 [Procedure Parameters and Arguments](/dotnet/visual-basic/language-reference/procedures/procedure-parameters-and-arguments)