---
title: "Error in project-level import &#39;&lt;qualifiedelementname&gt;&#39; at &#39;&lt;qualifiedcontainername&gt;&#39; : &lt;errormessage&gt; | Microsoft Docs"
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
  - "BC30797"
  - "vbc30797"
helpviewer_keywords: 
  - "BC30797"
ms.assetid: 529f354f-f255-4adc-ab21-bd1796e58d69
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
# Error in project-level import &#39;&lt;qualifiedelementname&gt;&#39; at &#39;&lt;qualifiedcontainername&gt;&#39; : &lt;errormessage&gt;
A statement accesses a programming element that is defined in another assembly, but there is no project reference to that assembly.  
  
 For example, your code might be accessing an enumeration named `desiredEnumeration` using the qualification string `otherNamespace.otherClass.desiredEnumeration`. If the compiler cannot find `otherNamespace.otherClass` among your project's references, it generates this error.  
  
 **Error ID:** BC30797  
  
### To correct this error  
  
1.  Make sure every element in the qualification string of the programming element is spelled correctly.  
  
2.  Make sure your project has a reference to the assembly defining the desired programming element.  
  
3.  Consult the error message and take appropriate action.  
  
## See Also  
 [NOTINBUILD: Resolving a Reference When Multiple Variables Have the Same Name](http://msdn.microsoft.com/en-us/9601e39f-1911-44e1-ace5-3f6e090408b9)   
 [NIB How to: Modify Project Properties and Configuration Settings](http://msdn.microsoft.com/en-us/e7184bc5-2f2b-4b4f-aa9a-3ecfcbc48b67)   
 [NIB How to: Add or Remove References By Using the Add Reference Dialog Box](http://msdn.microsoft.com/en-us/3bd75d61-f00c-47c0-86a2-dd1f20e231c9)