---
title: "Compiler Error CS1023 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS1023"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1023"
ms.assetid: 27d70f2c-9ae1-459c-a6be-01ed5a3eea07
caps.latest.revision: 6
author: "BillWagner"
ms.author: "wiwagn"
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
# Compiler Error CS1023
Embedded statement cannot be a declaration or labeled statement  
  
 An embedded statement, such as the statements following an **if** statement, can contain neither declarations nor labeled statements.  
  
 The following sample generates CS1023 twice:  
  
```  
// CS1023.cs  
public class a  
{  
   public static void Main()  
   {  
      if (1)  
         int i;      // CS1023, declaration is not valid here  
  
      if (1)  
         xx : i++;   // CS1023, labeled statement is not valid here  
   }  
}  
```