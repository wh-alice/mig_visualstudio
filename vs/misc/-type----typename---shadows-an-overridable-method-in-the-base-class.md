---
title: "&lt;type&gt; &#39;&lt;typename&gt;&#39; shadows an overridable method in the base class | hehe"
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
  - "vbc40005"
  - "bc40005"
helpviewer_keywords: 
  - "BC40005"
ms.assetid: 1dadda7f-1d26-4ae8-a668-9f69d55ceb50
caps.latest.revision: 11
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
# &lt;type&gt; &#39;&lt;typename&gt;&#39; shadows an overridable method in the base class
\<type> '\<typename>' shadows an overridable method in the base class. If you want to override the base method, this method must be declared 'Overrides'.  
  
 A programming element is declared with the same name as an overridable procedure or property defined in the base class. In this situation, the element in this class should shadow the base class element.  
  
 By default, this message is a warning. For more information about hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../ide/configuring-warnings-in-visual-basic.md).  
  
 **Error ID:** BC40005  
  
### To correct this error  
  
-   If you intend to override the base procedure, add the `Overrides` keyword to the declaration.  
  
-   If you intend to shadow the base procedure, add the `Shadows` keyword to the declaration.  
  
-   If you do not intend either overriding or shadowing, change the name of the element being declared.  
  
## See Also  
 [NOT IN BUILD: Overriding Properties and Methods](http://msdn.microsoft.com/en-us/2167e8f5-1225-4b13-9ebd-02591ba90213)   
 [Shadowing in Visual Basic](../Topic/Shadowing%20in%20Visual%20Basic.md)   
 [Overrides](../Topic/Overrides%20\(Visual%20Basic\).md)   
 [Shadows](../Topic/Shadows%20\(Visual%20Basic\).md)