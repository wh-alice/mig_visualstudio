---
title: "&#39;=&#39; expected (object initializer) | testtitle"
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
  - "vbc30984"
  - "bc30984"
helpviewer_keywords: 
  - "BC30984"
ms.assetid: 9cae8d32-775a-414f-9e51-0469974b6aab
caps.latest.revision: 9
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
# &#39;=&#39; expected (object initializer)
To establish the initial value for a field or property in an object initializer declaration, you must use an equal sign. For example, the following declaration assigns "Microsoft" as the initial value for the `Name` property of `client`.  
  
```  
Dim client As New Customer { .Name = "Microsoft" }  
```  
  
 **Error ID:** BC30984  
  
### To correct this error  
  
-   Add an equal sign in the position shown in the previous example.  
  
## See Also  
 [Object Initializers: Named and Anonymous Types](../Topic/Object%20Initializers:%20Named%20and%20Anonymous%20Types%20\(Visual%20Basic\).md)   
 [NOT IN BUILD: Properties and Property Procedures](http://msdn.microsoft.com/en-us/23e2a1ec-7e9d-4109-8940-c703d981077b)   
 [NOT IN BUILD: Property Procedures vs. Fields](http://msdn.microsoft.com/en-us/da1c05c1-87c7-40fa-b92c-e9c7e4d170f7)