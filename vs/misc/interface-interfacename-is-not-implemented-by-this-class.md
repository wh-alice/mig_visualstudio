---
title: "Interface &#39;&lt;interfacename&gt;&#39; is not implemented by this class | Microsoft Docs"
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
  - "bc31035"
  - "vbc31035"
helpviewer_keywords: 
  - "BC31035"
ms.assetid: 99ddabb5-20e0-4cf6-a8d4-1ca91f3c7511
caps.latest.revision: 9
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
# Interface &#39;&lt;interfacename&gt;&#39; is not implemented by this class
A member of this class or structure attempts to implement a member of an interface that the class or structure does not implement.  
  
 **Error ID:** BC31035  
  
### To correct this error  
  
-   Add an `Implements` statement at the beginning of the class or structure so that it implements the appropriate interface.  
  
-   Remove the `Implements` keyword from the member that causes this error.  
  
## See Also  
 [Interfaces](/dotnet/visual-basic/programming-guide/language-features/interfaces/index)   
 [Implements](/dotnet/visual-basic/language-reference/statements/implements-clause)   
 [Implements Statement](/dotnet/visual-basic/language-reference/statements/implements-statement)