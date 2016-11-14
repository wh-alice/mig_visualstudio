---
title: "Method &#39;&lt;methodname&gt;&#39; has a link demand, but overrides or implements the following methods which do not have a link demand. A security hole may exist: | Microsoft Docs"
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
  - "bc42200"
  - "vbc42200"
helpviewer_keywords: 
  - "BC42200"
ms.assetid: c79d672e-638c-4d87-9b93-edf12ce84a52
caps.latest.revision: 10
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
# Method &#39;&lt;methodname&gt;&#39; has a link demand, but overrides or implements the following methods which do not have a link demand. A security hole may exist:
A security link demand action has been added to the method. However, the method overrides or implements methods that do not have link demands. Therefore the overridden or implemented methods can be called with insufficient permissions, which may cause a security issue.  
  
 By default, this message is a warning. For more information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../ide/configuring-warnings-in-visual-basic.md).  
  
 **Error ID:** BC42200  
  
### To correct this error  
  
-   Add link demands to the overridden and/or implemented methods.  
  
## See Also  
 [Link Demands](http://msdn.microsoft.com/en-us/Library/a33fd5f9-2de9-4653-a4f0-d9df25082c4d)   
 [Demand vs. LinkDemand](http://msdn.microsoft.com/en-us/1ab877f2-70f4-4e0d-8116-943999dfe8f5)   
 [Security Optimizations](http://msdn.microsoft.com/en-us/cf255069-d85d-4de3-914a-e4625215a7c0)