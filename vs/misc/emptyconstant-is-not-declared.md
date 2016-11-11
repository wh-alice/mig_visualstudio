---
title: "&#39;&lt;emptyconstant&gt;&#39; is not declared | Microsoft Docs"
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
  - "bc30823"
  - "vbc30823"
helpviewer_keywords: 
  - "BC30823"
ms.assetid: 6e1b4f7f-e483-44c5-a550-ec152bfb7a55
caps.latest.revision: 15
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# &#39;&lt;emptyconstant&gt;&#39; is not declared
'\<emptyconstant>' is not declared. Empty constant is no longer supported; use Nothing instead.  
  
 A declaration or assignment statement attempts to assign a value of `Empty` to a variable, constant, enumeration member, property, or function return.  
  
 Previous versions of [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] used the `Empty` keyword to represent uninitialized data storage. The current version of Visual Basic does not support `Empty`. An uninitialized variable holds the default value for its data type. For more information about default values, see "Default Values" in [Dim Statement](/dotnet/visual-basic/language-reference/statements/dim-statement).  
  
 The [Nothing](/dotnet/visual-basic/language-reference/nothing) keyword represents the default value of any data type. You can use it instead of `Empty`.  
  
 **Error ID:** BC30823  
  
### To correct this error  
  
-   Use `Nothing` instead of `Empty`.  
  
     -or-  
  
-   Use the default value appropriate for the data type of the programming element.  
  
     -or-  
  
-   If this is a variable declaration, do not assign an initial value. This causes the variable to be initialized to its default value.  
  
## See Also  
 [Nothing](/dotnet/visual-basic/language-reference/nothing)   
 [Programming Element Support Changes Summary](http://msdn.microsoft.com/en-us/0483590a-6309-449c-a2fa-effa26a03b95)