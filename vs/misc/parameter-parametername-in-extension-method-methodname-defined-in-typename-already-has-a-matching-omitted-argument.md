---
title: "Parameter &#39;&lt;parametername&gt;&#39; in extension method &#39;&lt;methodname&gt;&#39; defined in &#39;&lt;typename&gt;&#39; already has a matching omitted argument | Microsoft Docs"
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
  - "bc36583"
  - "vbc36583"
helpviewer_keywords: 
  - "BC36583"
ms.assetid: 662072fa-abb8-43c3-8ca2-aefb20f2e902
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
# Parameter &#39;&lt;parametername&gt;&#39; in extension method &#39;&lt;methodname&gt;&#39; defined in &#39;&lt;typename&gt;&#39; already has a matching omitted argument
A procedure call to an extension method omits an argument by position and then supplies the argument by name. For example, the following call to extension method `ABC` first omits an argument for parameter `Y`, and then supplies it by name.  
  
```  
<Extension()> _  
Public Sub ABC(ByVal X As Integer, Optional ByVal Y As Byte = 0, _  
               Optional ByVal Z As Byte = 0)  
End Sub  
' . . .  
' Calling extension method ABC.  
Dim number As Integer  
' Not valid.  
' number.ABC(, 4, Y:=5)  
```  
  
 **Error ID:** BC36583  
  
### To correct this error  
  
-   Supply the argument by position, or remove the comma that omits it.  
  
## See Also  
 [Extension Methods](/dotnet/visual-basic/language-reference/procedures/extension-methods)   
 [Passing Arguments by Position and by Name](/dotnet/visual-basic/language-reference/procedures/passing-arguments-by-position-and-by-name)