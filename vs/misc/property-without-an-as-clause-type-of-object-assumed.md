---
title: "Property without an &#39;As&#39; clause; type of Object assumed | Microsoft Docs"
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
  - "BC42022"
  - "vbc42022"
helpviewer_keywords: 
  - "BC42022"
ms.assetid: 3379692b-8278-4488-878a-0afb76e554b1
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
# Property without an &#39;As&#39; clause; type of Object assumed
A property declaration does not specify an `As` clause.  
  
 An `As` clause identifies a data type to be associated with a programming element. In a [Property Statement](/dotnet/visual-basic/language-reference/statements/property-statement), it specifies the data type of the value that the property's `Get` procedure returns to the calling code. If you do not include an `As` clause in the `Property` statement, the property's data type defaults to `Object`.  
  
 By default, this message is a warning. For more information about hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../ide/configuring-warnings-in-visual-basic.md).  
  
 **Error ID:** BC42022  
  
### To correct this error  
  
-   Include an `As` clause in the `Property` statement to specify the property's data type.  
  
## See Also  
 [Property Procedures](/dotnet/visual-basic/language-reference/procedures/property-procedures)   
 [Property Statement](/dotnet/visual-basic/language-reference/statements/property-statement)   
 [Get Statement](/dotnet/visual-basic/language-reference/statements/get-statement)