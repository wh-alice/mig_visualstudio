---
title: "&#39;Class_Initialize&#39; event is no longer supported"
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
  - "vbc42001"
  - "bc42001"
helpviewer_keywords: 
  - "BC42001"
ms.assetid: 31e7c383-894e-416c-b834-3688cc340ccf
caps.latest.revision: 11
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
# &#39;Class_Initialize&#39; event is no longer supported
'Class_Initialize' event is no longer supported. Use 'Sub New' to initialize a class.  
  
 The `Class_Initialize` event of previous versions of [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] is replaced by class constructors.  
  
 By default, this message is a warning. For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../ide/configuring-warnings-in-visual-basic.md).  
  
 **Error ID:** BC42001  
  
### To correct this error  
  
-   Declare one or more `Sub` procedures named `New` to initialize a class. `Sub New` is called when a class instance is newly created.  
  
## See Also  
 [Class_Initialize Changes in Visual Basic](http://msdn.microsoft.com/en-us/2cd023cf-2869-4836-b08d-43822294beeb)   
 [Classes for Visual Basic 6.0 Users](http://msdn.microsoft.com/en-us/d625222c-cd32-4c8d-b25c-ea71729b88b7)   
 [NOT IN BUILD: Using Constructors and Destructors](http://msdn.microsoft.com/en-us/548eebe1-86c4-4377-b2f5-447cb8be3d90)