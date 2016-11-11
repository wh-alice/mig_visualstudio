---
title: "&#39;&lt;keyword&gt;&#39; is not valid within a Module | Microsoft Docs"
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
  - "vbc32001"
  - "bc32001"
helpviewer_keywords: 
  - "BC32001"
ms.assetid: b00757ac-5652-460d-9d2c-11b264d7ec7f
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
# &#39;&lt;keyword&gt;&#39; is not valid within a Module
A keyword related to class instances, such as `Me` or `MyBase`, is used inside a module. Modules do not have inheritance or instances.  
  
 **Error ID:** BC32001  
  
### To correct this error  
  
-   If the code using the keyword involves class instances, move it to a class implementation.  
  
-   If the code using the keyword applies to the module, remove the invalid keyword.  
  
## See Also  
 [Me](http://msdn.microsoft.com/en-us/a65973c7-cf06-4547-9b25-9fba885525c2)   
 [MyBase - delete](http://msdn.microsoft.com/en-us/52491d06-6451-4f6f-9aa6-8fab59bbc2b9)