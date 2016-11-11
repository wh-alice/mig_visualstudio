---
title: "Type &#39;&lt;typeName&gt;&#39; must be a value type or a type argument constrained to &#39;Structure&#39; in order to be used with &#39;Nullable&#39; or nullable modifier &#39;?&#39; | Microsoft Docs"
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
  - "vbc33101"
  - "bc33101"
helpviewer_keywords: 
  - "BC33101"
ms.assetid: b3e0e4e4-87b8-4a38-a450-15233497acaa
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
# Type &#39;&lt;typeName&gt;&#39; must be a value type or a type argument constrained to &#39;Structure&#39; in order to be used with &#39;Nullable&#39; or nullable modifier &#39;?&#39;
Only value types, including structures, can be declared nullable.  
  
```vb#  
' Valid.  
Dim n? As Integer  
Dim m As Integer?  
  
' Not valid.  
' Dim p? As Object  
' Dim q As Nullable(Of Object)  
```  
  
 **Error ID:** BC33101  
  
### To correct this error  
  
-   Remove the '?' or `Nullable`.  
  
-   Use a value data type.  
  
## See Also  
 [Nullable Value Types](/dotnet/visual-basic/programming-guide/language-features/data-types/nullable-value-types)