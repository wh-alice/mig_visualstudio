---
title: "Compiler Error CS1013"
ms.custom: ""
ms.date: "10/25/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS1013"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1013"
ms.assetid: e5b1d24d-e558-4f7c-b2b1-3a644710005d
caps.latest.revision: 8
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
# Compiler Error CS1013
Invalid number  
  
 The compiler detected a malformed number. For more information on integral types, see the [Integral Types Table](../Topic/Integral%20Types%20Table%20\(C%23%20Reference\).md).  
  
## Example  
 The following sample generates CS1013:  
  
```  
// CS1013.cs  
class Sample  
{  
    static void Main()  
    {  
        int i = 0x;   // CS1013  
    }  
}  
```