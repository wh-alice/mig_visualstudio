---
title: "Option Strict On does not allow narrowing in implicit type conversions between extension method &#39;&lt;extensionmethodname&gt;&#39; defined in &#39;&lt;modulename&gt;&#39; and delegate &#39;&lt;delegatename&gt;&#39; | Microsoft Docs"
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
  - "bc36709"
  - "vbc36709"
helpviewer_keywords: 
  - "BC36709"
ms.assetid: 95d8c833-3525-411b-98e8-b7d3f61f75c9
caps.latest.revision: 5
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
# Option Strict On does not allow narrowing in implicit type conversions between extension method &#39;&lt;extensionmethodname&gt;&#39; defined in &#39;&lt;modulename&gt;&#39; and delegate &#39;&lt;delegatename&gt;&#39;
With `Option Strict` on, you cannot have a narrowing conversion from the data type of a parameter in a delegate to the corresponding parameter of an extension method assigned to a variable of that delegate type. The data type of the delegate parameter must widen to the data type of the extension method.  
  
 **Error ID:** BC36709  
  
### To correct this error  
  
-   Change the data type of the parameter in the delegate or the extension method so that the required widening relationship exists.  
  
## See Also  
 [Extension Methods](/dotnet/visual-basic/language-reference/procedures/extension-methods)   
 [Relaxed Delegate Conversion](/dotnet/visual-basic/programming-guide/language-features/delegates/relaxed-delegate-conversion)   
 [Delegates](/dotnet/visual-basic/programming-guide/language-features/delegates/delegates)   
 [Widening and Narrowing Conversions](/dotnet/visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions)   
 [NOT IN BUILD: Delegates and the AddressOf Operator](http://msdn.microsoft.com/en-us/7b2ed932-8598-4355-b2f7-5cedb23ee86f)