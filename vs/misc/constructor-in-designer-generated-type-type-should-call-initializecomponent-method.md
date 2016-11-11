---
title: "&#39;&lt;constructor&gt;&#39; in designer-generated type &#39;&lt;type&gt;&#39; should call InitializeComponent method | Microsoft Docs"
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
  - "vbc40054"
  - "bc40054"
helpviewer_keywords: 
  - "BC40054"
ms.assetid: beac93b0-d427-4df6-9582-fd69c7a53673
caps.latest.revision: 7
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
# &#39;&lt;constructor&gt;&#39; in designer-generated type &#39;&lt;type&gt;&#39; should call InitializeComponent method
A constructor in a designer-generated type does not call the type's `InitializeComponent` method.  
  
 Each constructor in a designer-generated type should call the type's `InitializeComponent` method.  
  
 **Error ID:** BC40054  
  
### To correct this error  
  
-   Add a call to the `InitializeComponent` method in the constructor.  
  
## See Also  
 <xref:Microsoft.VisualBasic.CompilerServices.DesignerGeneratedAttribute>   
 [NOT IN BUILD: Using Constructors and Destructors](http://msdn.microsoft.com/en-us/548eebe1-86c4-4377-b2f5-447cb8be3d90)