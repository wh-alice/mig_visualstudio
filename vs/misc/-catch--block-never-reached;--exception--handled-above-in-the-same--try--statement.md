---
title: "&#39;Catch&#39; block never reached; &lt;exception&gt; handled above in the same &#39;Try&#39; statement"
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
  - "bc42031"
  - "vbc42031"
helpviewer_keywords: 
  - "BC42031"
ms.assetid: 7d15597c-5988-42ea-a853-63cbf78faaf3
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
# &#39;Catch&#39; block never reached; &lt;exception&gt; handled above in the same &#39;Try&#39; statement
A `Catch` block in the code cannot be reached because it is handled in a preceding `Try` block.  
  
 By default, this message is a warning. For more information about hiding warnings or treating warnings as errors, please see [Configuring Warnings in Visual Basic](../ide/configuring-warnings-in-visual-basic.md)  
  
 **Error ID:** BC42031  
  
### To correct this error  
  
-   Remove the redundant statement.  
  
## See Also  
 [How to: Catch an Exception in Visual Basic](http://msdn.microsoft.com/f3063c89-d2bf-49b1-91b5-b87edfb18b95)   
 [How to: Test Code with a Try…Catch Block in Visual Basic](http://msdn.microsoft.com/8368e205-ed73-4185-a247-af84fb4fafa9)   
 [How to: Filter Errors in a Catch Block in Visual Basic](http://msdn.microsoft.com/85964d0a-56e7-4301-a96e-5eaea23b7b9b)   
 [Walkthrough: Structured Exception Handling (Visual Basic)](http://msdn.microsoft.com/440da655-4b32-490b-8b16-bfe46f41fa76)   
 [Try...Catch...Finally Statement](../Topic/Try...Catch...Finally%20Statement%20\(Visual%20Basic\).md)