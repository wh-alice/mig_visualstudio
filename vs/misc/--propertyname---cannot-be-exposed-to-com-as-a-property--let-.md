---
title: "&#39;&lt;propertyname&gt;&#39; cannot be exposed to COM as a property &#39;Let&#39;"
ms.custom: na
ms.date: "10/13/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "bc42102"
  - "vbc42102"
helpviewer_keywords: 
  - "BC42102"
ms.assetid: b77c5b7c-ac43-4b2d-b8bc-582e65e6f7e7
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
# &#39;&lt;propertyname&gt;&#39; cannot be exposed to COM as a property &#39;Let&#39;
'\<propertyname>' cannot be exposed to COM as a property 'Let'. You will not be able to assign non-object values (such as numbers or strings) to this property from Visual Basic 6.0 using a 'Let' statement.  
  
 A class using a `COMClassAttribute` attribute block declares a `Public` property with data type `Object`. A Visual Basic 6.0 program can access this property as a `Variant`, but can assign only an object reference to it with the `Set` statement. It cannot assign a value type with the `Let` statement.  
  
 By default, this message is a warning. For more information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../ide/configuring-warnings-in-visual-basic.md).  
  
 **Error ID:** BC42102  
  
### To address this warning  
  
-   Consider informing potential Visual Basic 6.0 users of this class that they cannot use this property with the `Let` statement.  
  
## See Also  
 [Default Property Changes in Visual Basic](http://msdn.microsoft.com/en-us/9b8cfad7-40ac-4b83-affb-1ff781755a4c)   
 [Property Statement](../Topic/Property%20Statement.md)   
 [Public](../Topic/Public%20\(Visual%20Basic\).md)   
 [Object Data Type](../Topic/Object%20Data%20Type.md)   
 [NOT IN BUILD: Attributes Used in Visual Basic](http://msdn.microsoft.com/en-us/22231318-8a40-49af-9245-e0aab723563b)   
 [NOT IN BUILD: Application of Attributes](http://msdn.microsoft.com/en-us/2b1703ed-4437-49b3-bc0b-568094324f47)   
 [ComClassAttribute Class](http://msdn.microsoft.com/en-us/5c2f0835-9210-47dc-bc59-5c1769953574)