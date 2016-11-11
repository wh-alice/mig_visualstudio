---
title: "Parameter &#39;&lt;parametername&gt;&#39; already has a matching omitted argument | Microsoft Docs"
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
  - "vbc36566"
  - "bc36566"
helpviewer_keywords: 
  - "BC36566"
ms.assetid: b37af6bc-abd0-4436-bf8a-a467e3603342
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
# Parameter &#39;&lt;parametername&gt;&#39; already has a matching omitted argument
A procedure call supplies an argument by name after omitting the same argument by position. Following is an example:  
  
```vb#  
Public Sub ABC(ByVal X As Byte, Optional ByVal Y As Byte = 0, _  
                                Optional ByVal Z As Byte = 0)  
' ...  
' Argument Y is omitted by position, but supplied by name.  
Call ABC(6, , Y:=3)     
```  
  
 **Error ID:** BC36566  
  
### To correct this error  
  
-   Supply the argument by position, or remove the comma that omits it.  
  
## See Also  
 [Passing Arguments by Position and by Name](/dotnet/visual-basic/language-reference/procedures/passing-arguments-by-position-and-by-name)