---
title: "&#39;Catch&#39; must end with a matching &#39;End Try&#39;"
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
  - "bc30441"
  - "vbc30441"
helpviewer_keywords: 
  - "BC30441"
ms.assetid: 0e4756b4-1f29-4073-88c5-8f8c93ba6c9e
caps.latest.revision: 7
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
# &#39;Catch&#39; must end with a matching &#39;End Try&#39;
A `Catch` statement appears in your code without a matching `End Try` statement. `Catch` statements must be concluded with an `End Try` statement.  
  
 **Error ID:** BC30441  
  
### To correct this error  
  
1.  Remove the `Catch` statement.  
  
2.  Add an `End Try` statement to conclude the block.  
  
## See Also  
 [Try...Catch...Finally Statement](../Topic/Try...Catch...Finally%20Statement%20\(Visual%20Basic\).md)   
 [Structured Exception Handling Overview for Visual Basic](http://msdn.microsoft.com/en-us/bb81af80-a735-4873-9711-6151a48e418a)