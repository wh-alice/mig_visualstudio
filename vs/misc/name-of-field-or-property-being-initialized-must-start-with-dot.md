---
title: "Name of field or property being initialized must start with &#39;.&#39; | Microsoft Docs"
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
  - "vbc30985"
  - "bc30985"
helpviewer_keywords: 
  - "BC30985"
ms.assetid: 4cb543e1-477c-429c-82df-541ebff08543
caps.latest.revision: 7
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
# Name of field or property being initialized must start with &#39;.&#39;
Each member initializer in an object initializer list specifies the name of a field or property and its initial value. The name of the field or property must be preceded by a period. For example, the following declaration assigns "Microsoft" as the initial value for the `Name` property of `client`.  
  
```  
Dim client As New Customer() With { .Name = "Microsoft" }  
```  
  
 **Error ID:** BC30985  
  
### To correct this error  
  
-   Prefix each member name with a period.  
  
## See Also  
 [Object Initializers: Named and Anonymous Types](http://msdn.microsoft.com/en-us/Library/e2df3807-a70f-49dd-ac94-f1e07f472b1b)   
 [NOT IN BUILD: Property Procedures vs. Fields](http://msdn.microsoft.com/en-us/da1c05c1-87c7-40fa-b92c-e9c7e4d170f7)