---
title: "Attribute specifier is not a complete statement"
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
  - "vbc32035"
  - "bc32035"
helpviewer_keywords: 
  - "BC32035"
ms.assetid: a0ddd673-4170-4bea-9c22-777d7bf21dfd
caps.latest.revision: 10
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
# Attribute specifier is not a complete statement
Attribute specifier is not a complete statement. Use a line continuation to apply the attribute to the following statement.  
  
 An attribute block appears alone on a source-code line. Attributes must be applied at the beginning of a declaration statement, and they must be part of that statement.  
  
 **Error ID:** BC32035  
  
### To correct this error  
  
-   If the declaration statement is on the following line, add a space and an underscore (`_`) following the attribute block to combine the source-code lines.  
  
-   If no declaration statement is associated with the attribute block, either supply one or remove the attribute block.  
  
-   If the attribute is to apply to the entire assembly or to the current assembly module, the attribute block remains on a separate source-code line. Precede the attribute name inside the angle brackets (`< >`) with `Assembly:` or `Module:` and do not add a space or underscore following the attribute block. Also, be sure this attribute block is at the beginning of your source file.  
  
## See Also  
 [NOT IN BUILD: Application of Attributes](http://msdn.microsoft.com/en-us/2b1703ed-4437-49b3-bc0b-568094324f47)   
 [How to: Break and Combine Statements in Code](../Topic/How%20to:%20Break%20and%20Combine%20Statements%20in%20Code%20\(Visual%20Basic\).md)