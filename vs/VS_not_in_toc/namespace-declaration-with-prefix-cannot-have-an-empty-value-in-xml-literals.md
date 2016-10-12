---
title: "Namespace declaration with prefix cannot have an empty value in XML literals"
ms.custom: na
ms.date: "10/01/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "bc31184"
  - "vbc31184"
helpviewer_keywords: 
  - "BC31184"
ms.assetid: dde656b4-df3b-4a2e-8871-4e14832ca778
caps.latest.revision: 6
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
# Namespace declaration with prefix cannot have an empty value in XML literals
An XML namespace declaration in an XML literal does not include a namespace value. For example, the following code will cause this error:  
  
```vb#  
Dim book = <book xmlns:ns=""/>  
```  
  
 **Error ID:** BC31184  
  
### To correct this error  
  
-   Include a valid namespace in the XML namespace declaration, or remove the XML namespace declaration from the XML literal.  
  
     As an alternative, you can use the `Imports` statement to identify a namespace prefix for the empty namespace. For example:  
  
    ```vb#  
    Imports <xmlns:ns="">  
    ```  
  
## See Also  
 [XML Literals](../Topic/XML%20Literals%20\(Visual%20Basic\).md)   
 [XML](../Topic/XML%20in%20Visual%20Basic.md)   
 [Imports Statement (XML Namespace)](../Topic/Imports%20Statement%20\(XML%20Namespace\).md)