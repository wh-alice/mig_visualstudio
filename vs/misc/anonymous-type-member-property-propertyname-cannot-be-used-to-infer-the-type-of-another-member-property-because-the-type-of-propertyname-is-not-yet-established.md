---
title: "Anonymous type member property &#39;&lt;propertyname&gt;&#39; cannot be used to infer the type of another member property because the type of &#39;&lt;propertyname&gt;&#39; is not yet established | Microsoft Docs"
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
  - "vbc36559"
  - "bc36559"
helpviewer_keywords: 
  - "BC36559"
ms.assetid: 58ab8d35-9d85-4aca-8b4e-f232d7e4af61
caps.latest.revision: 6
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
# Anonymous type member property &#39;&lt;propertyname&gt;&#39; cannot be used to infer the type of another member property because the type of &#39;&lt;propertyname&gt;&#39; is not yet established
Until the type of an anonymous type property is established, it cannot be used to establish the type of another property. For example, in the following declaration `.IDName = .LastName` is not valid because `.LastName` has not yet been initialized.  
  
```  
' Not valid.   
' Dim anon1 = New With {Key .IDName = .LastName, Key .LastName = "Jones"}   
```  
  
 **Error ID:** BC36559  
  
### To correct this error  
  
-   Establish the type of the property before using it to initialize another property.  
  
    ```  
    Dim anon2 = New With {Key .LastName = "Jones", Key .IDName = .LastName}  
    ```  
  
## See Also  
 [Anonymous Types](/dotnet/visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types)   
 [How to: Infer Property Names and Types in Anonymous Type Declarations](http://msdn.microsoft.com/en-us/Library/7c748b22-913f-4d9d-b747-6b7bf296a0bc)