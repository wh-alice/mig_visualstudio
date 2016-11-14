---
title: "&#39;WriteOnly&#39; properties cannot have an access modifier on &#39;Set&#39; | Microsoft Docs"
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
  - "bc31104"
  - "vbc31104"
helpviewer_keywords: 
  - "BC31104"
ms.assetid: d1ac04a8-e436-4f3e-8d71-fc4569b35fcd
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
# &#39;WriteOnly&#39; properties cannot have an access modifier on &#39;Set&#39;
A `WriteOnly` property declaration specifies access levels in both the [Property Statement](/dotnet/visual-basic/language-reference/statements/property-statement) and the [Set Statement](/dotnet/visual-basic/language-reference/statements/set-statement).  
  
 You can always specify an access level for the property. In addition, you can specify a different access level for at most one of its property procedures (`Get` or `Set`), provided it is more restrictive than the property's access level. You cannot specify access levels for both of the property procedures.  
  
 **Error ID:** BC31104  
  
### To correct this error  
  
-   Remove the access modifier from the `Set` statement. It represents the entire `WriteOnly` property, and you cannot have two access levels for the property.  
  
## See Also  
 [Property Procedures](/dotnet/visual-basic/language-reference/procedures/property-procedures)   
 [How to: Declare a Property with Mixed Access Levels](http://msdn.microsoft.com/en-us/Library/fdbb2d97-279a-4956-b26c-cbdfbc34915a)