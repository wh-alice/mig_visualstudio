---
title: "Methods in a Module cannot be declared &#39;&lt;specifier&gt;&#39; | Microsoft Docs"
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
  - "bc30433"
  - "vbc30433"
helpviewer_keywords: 
  - "BC30433"
ms.assetid: e9fa204c-a40f-439e-95bb-048a89a19159
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
# Methods in a Module cannot be declared &#39;&lt;specifier&gt;&#39;
You have used a specifier that is not valid on a method within a `Module` statement. Modules can never be instantiated, do not support inheritance, and cannot implement interfaces.  
  
 **Error ID:** BC30433  
  
### To correct this error  
  
-   Remove the specifier.  
  
## See Also  
 [Module Statement](/dotnet/visual-basic/language-reference/statements/module-statement)