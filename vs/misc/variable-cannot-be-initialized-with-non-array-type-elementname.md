---
title: "Variable cannot be initialized with non-array type &#39;&lt;elementname&gt;&#39; | Microsoft Docs"
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
  - "vbc36536"
  - "bc36536"
helpviewer_keywords: 
  - "BC36536"
ms.assetid: 959415de-164e-4971-aab0-faad315753e9
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
# Variable cannot be initialized with non-array type &#39;&lt;elementname&gt;&#39;
A variable that is declared as an array must be initialized with an array value.  
  
```  
' Not valid.  
' The following line causes this error when executed with Option Strict off.  
' Dim arrayVar1() = 10  
```  
  
 **Error ID:** BC36536  
  
### To correct this error  
  
-   Initialize the array variable with an array value:  
  
    ```  
    ' With Option Strict off.  
    Dim arrayVar2() = {1, 2, 3}  
    ' With Option Strict on.  
    Dim arrayVar3() As Integer = {1, 2, 3}  
    ```  
  
## See Also  
 [NOTINBUILD  an Array Variable](http://msdn.microsoft.com/en-us/c2da78bd-6928-46ba-805f-44f819dfaf93)