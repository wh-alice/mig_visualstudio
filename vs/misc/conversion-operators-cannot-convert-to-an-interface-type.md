---
title: "Conversion operators cannot convert to an interface type | Microsoft Docs"
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
  - "vbc33025"
  - "bc33025"
helpviewer_keywords: 
  - "BC33025"
ms.assetid: 7e13dfa3-2b70-4ca6-a8ec-159131fd2c4c
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
# Conversion operators cannot convert to an interface type
A conversion operator is declared with an interface type as a return type.  
  
 At compile time, [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] considers a predefined conversion to exist from any reference type to any interface. Such a conversion might fail at run time, but the compiler cannot predict run-time results, so it allows any such conversion to compile.  
  
 Because the compiler considers this conversion to be already defined, it does not allow you to redefine it.  
  
 **Error ID:** BC33025  
  
### To correct this error  
  
-   Remove this operator definition entirely. It is already predefined.  
  
## See Also  
 [Operator Procedures](/dotnet/visual-basic/language-reference/procedures/operator-procedures)   
 [Operator Statement](/dotnet/visual-basic/language-reference/statements/operator-statement)   
 [How to: Define an Operator](http://msdn.microsoft.com/en-us/Library/d4b0e253-092a-4e6e-9fe2-01f562140a29)   
 [How to: Define a Conversion Operator](http://msdn.microsoft.com/en-us/Library/54203dfa-c24b-463f-9942-d5153e89e762)