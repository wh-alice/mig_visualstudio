---
title: "&#39;Exit Operator&#39; is not valid. Use &#39;Return&#39; to exit an Operator | Microsoft Docs"
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
  - "bc33008"
  - "vbc33008"
helpviewer_keywords: 
  - "BC33008"
ms.assetid: 8c44456b-8fd2-4168-ad8c-b6da129242ba
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
# &#39;Exit Operator&#39; is not valid. Use &#39;Return&#39; to exit an Operator
An `Exit Operator` statement appears in an `Operator` procedure.  
  
 You must use a [Return Statement](/dotnet/visual-basic/language-reference/statements/return-statement) to return from an `Operator` procedure. The [Exit Statement](/dotnet/visual-basic/language-reference/statements/exit-statement) does not accept the `Operator` keyword, and the `End Operator` statement does not return control to the calling code.  
  
 **Error ID:** BC33008  
  
### To correct this error  
  
-   Replace the `Exit Operator` statement with a `Return` statement.  
  
## See Also  
 [Operator Procedures](/dotnet/visual-basic/language-reference/procedures/operator-procedures)   
 [Operator Statement](/dotnet/visual-basic/language-reference/statements/operator-statement)   
 [How to: Define an Operator](http://msdn.microsoft.com/en-us/Library/d4b0e253-092a-4e6e-9fe2-01f562140a29)   
 [How to: Define a Conversion Operator](http://msdn.microsoft.com/en-us/Library/54203dfa-c24b-463f-9942-d5153e89e762)