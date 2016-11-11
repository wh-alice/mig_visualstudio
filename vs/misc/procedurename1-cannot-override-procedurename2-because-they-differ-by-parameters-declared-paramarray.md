---
title: "&lt;procedurename1&gt; cannot override &lt;procedurename2&gt; because they differ by parameters declared &#39;ParamArray&#39; | Microsoft Docs"
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
  - "bc30906"
  - "vbc30906"
helpviewer_keywords: 
  - "BC30906"
ms.assetid: 12939030-732e-4c6d-8fe9-707b7532174b
caps.latest.revision: 11
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
# &lt;procedurename1&gt; cannot override &lt;procedurename2&gt; because they differ by parameters declared &#39;ParamArray&#39;
A procedure in a derived class overrides an identically named procedure in the base class, but the parameter lists are different.  
  
 To override a procedure in an inherited class, the overriding procedure must match its parameter list, access level, and return type (if any). In particular, it must match any [Optional](/dotnet/visual-basic/language-reference/modifiers/optional) or [ParamArray](/dotnet/visual-basic/language-reference/modifiers/paramarray) declaration.  
  
 **Error ID:** BC30906  
  
### To correct this error  
  
-   If you want to override the procedure, make the parameter list exactly the same as the parameter list in the base class procedure. If the last parameter is declared with `ParamArray` in the base class procedure, declare it with `ParamArray` in the overriding procedure.  
  
-   If you want a different parameter list from the base class version, you cannot override it. Consider overloading it instead. For more information, see [Procedure Overloading](/dotnet/visual-basic/language-reference/procedures/procedure-overloading).  
  
## See Also  
 [Overrides](/dotnet/visual-basic/language-reference/modifiers/overrides)   
 [NOT IN BUILD: Overriding Properties and Methods](http://msdn.microsoft.com/en-us/2167e8f5-1225-4b13-9ebd-02591ba90213)