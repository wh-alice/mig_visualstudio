---
title: "&#39;&lt;emptyconstant&gt;&#39; is not declared"
ms.custom: na
ms.date: "10/10/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "bc30823"
  - "vbc30823"
helpviewer_keywords: 
  - "BC30823"
ms.assetid: 6e1b4f7f-e483-44c5-a550-ec152bfb7a55
caps.latest.revision: 13
ms.author: "billchi"
manager: "douge"
---
# &#39;&lt;emptyconstant&gt;&#39; is not declared
'\<emptyconstant>' is not declared. Empty constant is no longer supported; use Nothing instead.  
  
 A declaration or assignment statement attempts to assign a value of `Empty` to a variable, constant, enumeration member, property, or function return.  
  
 Previous versions of [!INCLUDE[vbprvb](../codequality/includes/vbprvb_md.md)] used the `Empty` keyword to represent uninitialized data storage. [!INCLUDE[vb_current_long]()] does not support `Empty`. An uninitialized variable holds the default value for its data type. For more information about default values, see "Default Values" in [Dim Statement](../Topic/Dim%20Statement%20\(Visual%20Basic\).md).  
  
 The [Nothing](../Topic/Nothing%20\(Visual%20Basic\).md) keyword represents the default value of any data type. You can use it instead of `Empty`.  
  
 **Error ID:** BC30823  
  
### To correct this error  
  
-   Use `Nothing` instead of `Empty`.  
  
     -or-  
  
-   Use the default value appropriate for the data type of the programming element.  
  
     -or-  
  
-   If this is a variable declaration, do not assign an initial value. This causes the variable to be initialized to its default value.  
  
## See Also  
 [Nothing](../Topic/Nothing%20\(Visual%20Basic\).md)   
 [Programming Element Support Changes Summary](http://msdn.microsoft.com/0483590a-6309-449c-a2fa-effa26a03b95)