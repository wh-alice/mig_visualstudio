---
title: "XML literal cannot appear here unless it is enclosed in parentheses | hehe"
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
  - "bc31198"
  - "vbc31198"
helpviewer_keywords: 
  - "BC31198"
ms.assetid: 97b16076-39ff-430a-9c65-073d01bcb08e
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
# XML literal cannot appear here unless it is enclosed in parentheses
An XML literal declaration is used in an expression in a location that is ambiguous to the [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] compiler. That is, the [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] compiler cannot determine whether the less-than character (<) is intended as a comparative operator or the start of an XML literal. The following code provides an example:  
  
 [Visual Basic]  
  
```  
' Generates an error.  
Dim queryResult = From element In elements _  
                  Where <sample>Value</sample> = "Value" _  
                  Select element  
```  
  
 **Error ID:** BC31198  
  
### To correct this error  
  
-   Enclose the XML literal declaration in parentheses, as shown in the following example:  
  
    ```vb#  
    Dim queryResult = From element In elements _  
                      Where (<sample> Value</sample>) = "Value" _  
                      Select element  
    ```  
  
-   Modify your code to refer to an existing XML literal, as shown in the following example:  
  
    ```vb#  
    Dim queryResult = From element In elements _  
                      Where e.<sample>.Value = "Value" _  
                      Select element  
    ```  
  
## See Also  
 [XML Literals](../Topic/XML%20Literals%20\(Visual%20Basic\).md)   
 [XML Axis Properties](../Topic/XML%20Axis%20Properties%20\(Visual%20Basic\).md)   
 [XML](../Topic/XML%20in%20Visual%20Basic.md)