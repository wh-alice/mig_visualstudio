---
title: "Compiler Error CS0442 | Microsoft Docs"
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
  - "CS0442"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0442"
ms.assetid: a411660d-0db6-4b63-b19e-f4538fc201e5
caps.latest.revision: 10
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
# Compiler Error CS0442
'Property': abstract properties cannot have private accessors  
  
 This error occurs when you use the access modifier "private" to modify an abstract accessor. To resolve, use a different access modifier, or make the property non-abstract.  
  
## Example  
 The following sample generates CS0442:  
  
```  
// CS0442.cs  
public abstract class MyClass   
{  
    public abstract int AbstractProperty   
    {  
        get;  
        private set;   // CS0442  
        // Try this instead:  
        // set;  
    }  
}  
```