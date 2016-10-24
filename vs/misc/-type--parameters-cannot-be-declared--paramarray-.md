---
title: "&lt;type&gt; parameters cannot be declared &#39;ParamArray&#39;"
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
  - "bc33009"
  - "vbc33009"
helpviewer_keywords: 
  - "BC33009"
ms.assetid: faba9aef-ca4e-4c4d-934c-a3e3d3fa3c3e
caps.latest.revision: 8
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
# &lt;type&gt; parameters cannot be declared &#39;ParamArray&#39;
A definition of a delegate, event, or operator declares a [ParamArray](../Topic/ParamArray%20\(Visual%20Basic\).md) parameter.  
  
 `ParamArray` parameters are allowed only on `Declare`, `Function`, `Property`, and `Sub` parameters.  
  
 **Error ID:** BC33009  
  
### To correct this error  
  
-   Remove the `ParamArray` keyword from the parameter list.  
  
-   If you are defining an operator, you might be able to achieve the `ParamArray` functionality with a series of overloads.  
  
-   If you are defining a delegate or event, you must rework the overall logic of this part of your application. You cannot use [Optional](../Topic/Optional%20\(Visual%20Basic\).md) or `ParamArray` parameters, or overloaded versions, on delegate or event parameters.  
  
## See Also  
 [Overloads](../Topic/Overloads%20\(Visual%20Basic\).md)   
 [Operator Procedures](../Topic/Operator%20Procedures%20\(Visual%20Basic\).md)   
 [Operator Statement](../Topic/Operator%20Statement.md)