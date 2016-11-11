---
title: "Members in a Module cannot be declared &#39;&lt;specifier&gt;&#39; | Microsoft Docs"
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
  - "vbc30436"
  - "bc30436"
helpviewer_keywords: 
  - "BC30436"
ms.assetid: c0560864-64f6-4c76-803f-d9c51df89d62
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
# Members in a Module cannot be declared &#39;&lt;specifier&gt;&#39;
You have used a specifier that is not valid on a member within a `Module` statement. Modules can never be instantiated, do not support inheritance, and cannot implement interfaces.  
  
 **Error ID:** BC30436  
  
### To correct this error  
  
-   Remove the specifier.  
  
## See Also  
 [Module Statement](/dotnet/visual-basic/language-reference/statements/module-statement)