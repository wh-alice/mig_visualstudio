---
title: "&#39;Declare&#39; statements are not allowed in generic types or types contained in generic types | Microsoft Docs"
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
  - "BC32075"
  - "vbc32075"
helpviewer_keywords: 
  - "BC32075"
ms.assetid: c620b67e-70f8-42ac-8292-e9ea484904c3
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
# &#39;Declare&#39; statements are not allowed in generic types or types contained in generic types
A `Declare` statement appears as part of a generic class or structure, or a class or structure declared within a generic class or structure.  
  
 Visual Basic and the .NET Framework do not currently support any combination of external references and generic types. The compiler needs all the parameters and the return type of an external procedure to call it correctly.  
  
 **Error ID:** BC32075  
  
### To correct this error  
  
-   Move the `Declare` statement outside the scope of any generic type, or remove it altogether.  
  
## See Also  
 [Declare Statement](/dotnet/visual-basic/language-reference/statements/declare-statement)   
 [Generic Types in Visual Basic](/dotnet/visual-basic/programming-guide/language-features/data-types/generic-types)