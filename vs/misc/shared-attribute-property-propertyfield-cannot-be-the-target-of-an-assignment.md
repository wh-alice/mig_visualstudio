---
title: "&#39;Shared&#39; attribute property &#39;&lt;propertyfield&gt;&#39; cannot be the target of an assignment | Microsoft Docs"
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
  - "bc31500"
  - "vbc31500"
helpviewer_keywords: 
  - "BC31500"
ms.assetid: dffa2b07-9609-4aa3-ae58-c0804d8a05d6
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
# &#39;Shared&#39; attribute property &#39;&lt;propertyfield&gt;&#39; cannot be the target of an assignment
An attempt was made to assign a value to a `ReadOnly` or `Shared` property in an attribute.  
  
 **Error ID:** BC31500  
  
### To correct this error  
  
1.  Remove the property assignment statement.  
  
2.  If using properties you developed, remove the `ReadOnly` or `Shared` modifiers from the attribute property.  
  
## See Also  
 [Shared](/dotnet/visual-basic/language-reference/modifiers/shared)   
 [NOT IN BUILD: Attributes in Visual Basic](http://msdn.microsoft.com/en-us/620bfc0e-4582-4c8b-8432-ebc5c3dccc22)