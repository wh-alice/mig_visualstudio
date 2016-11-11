---
title: "&#39;#If&#39; block must end with a matching &#39;#End If&#39; | Microsoft Docs"
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
  - "vbc30012"
  - "bc30012"
helpviewer_keywords: 
  - "BC30012"
ms.assetid: 9d51f3be-d2c3-4918-a36d-0d9e9763e47b
caps.latest.revision: 10
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
# &#39;#If&#39; block must end with a matching &#39;#End If&#39;
`#If` is a conditional compilation directive. An `#If` block is not terminated by an `#End If` directive.  
  
 **Error ID:** BC30012  
  
### To correct this error  
  
-   Add an `#End If` directive to the end of the conditional compilation block.  
  
## See Also  
 [#If...Then...#Else Directives](/dotnet/visual-basic/language-reference/directives/if-then-else-directives)